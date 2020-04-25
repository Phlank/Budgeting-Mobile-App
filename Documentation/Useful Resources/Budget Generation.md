Budget Generation
=================

Setup Pages
-----------

User input for the first-time budget creation happens in the pages found in lib/view/pages/setup.

The order of the pages is a tree as follows:

```
Welcome Page
└── Personal Info Page
    └── Financial Info Page
        └── Savings Depletion Info Page
            └── Housing Info Page
                └── Pin Info Page
                    └── More Questions Page
                        ├── Setup Finished Page
                        └── Kids Pets Info Page
                            └── Setup Finished Page
```

The pages store the user input into a class called `SetupAgent` located in lib/model. In the `SetupFinishedPage`, a call to `BudgetControl.setup()` is made which then makes a call to `PriorityBudgetFactory.newFromInfo()`.

PriorityBudgetFactory
---------------------

All budget generation happens inside of this class. Budgets use the `AllocationList` data type to store information about money that is allotted and spent over time. The main purpose of the Budget is to provide central location for lots of data that builds over the month. At the end of each month, the budget is reset with an opportunity to automatically reallocate funds. This reallocation happens through the `PriorityBudgetFactory` with the `newMonthBudget(Budget old)` method. The `PriorityBudgetFactory` can also provide a new Budget through user info through `newFromInfo()`.

### Generating budgets from user-provided information

`SetupAgent` has a field for each option provided in the Setup pages. However, only three pertain to the creation of the `Budget` itself.

#### Budget Types

There are two budget types: `growth` and `depletion`. `depletion` operates by removing money from the savings each month to pay for expenses. If `depletion` is chosen during setup, no money will be allocated towards the `savings` priority. In `growth`, the opposite is true: Income is the only source of providing for the user, and money will be allocated to `savings`.

#### Tiers

There are four tiers of allocations, and all are dependent on the ratio of `housing percent = monthly housing cost / monthly income`. Each tier has three ratios which correspond to the ratio of monthly income to be allotted to three priorities. These priorities are:

-	Needs
-	Wants
-	Saving

The following is the table demonstrating how the ratio `housing percent` corresponds to the ratios of needs, wants, and savings in a `growth` budget.

| Housing percent |  | Needs | Wants | Savings |
|-----------------|--|-------|-------|---------|
| 0.3             |  | 0.5   | 0.3   | 0.2     |
| 0.55            |  | 0.75  | 0.15  | 0.2     |
| 0.7             |  | 0.85  | 0.1   | 0.05    |
| 1.0             |  | 0.94  | 0.05  | 0.01    |

The following is the same for `depletion`.

| Housing percent |  | Needs | Wants | Savings |
|-----------------|--|-------|-------|---------|
| 0.3             |  | 0.6   | 0.4   | 0.0     |
| 0.55            |  | 0.75  | 0.25  | 0.0     |
| 0.7             |  | 0.9   | 0.1   | 0.0     |
| 1.0             |  | 0.95  | 0.05  | 0.0     |

#### Making the allocation

With tiers in mind, allocations are fairly simple. Think of each `priority` as a list of categories, like Housing or Groceries.

##### Needs

There is one exceptional category in `needs`, and that's `housing`. `Housing` will always earn its full share of income no matter what, and the money that is left over in `needs` is divided evenly between all the other categories.

##### Wants

There are no exceptional categories in `wants`, so money is simply divided evenly between categories.

##### Savings

There is only one category here, so all money is allocated to that category.

### Generating a new budget for new months
