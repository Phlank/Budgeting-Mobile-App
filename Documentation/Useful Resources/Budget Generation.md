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

`SetupAgent` has a field for each option provided in the Setup pages. However, only two pertain to the creation of the `Budget` itself.

#### Tiers

There are four tiers of allocations, and all are dependent on the ratio of `housing percent = monthly housing cost / monthly income`. Each tier has three ratios which correspond to the ratio of monthly income to be allotted to three priorities. These priorities are:

-	Needs
-	Wants
-	Saving

The following is a table demonstrating how the ratio `housing percent` corresponds to the ratios of needs, wants, and savings.
