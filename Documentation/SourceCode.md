In-line code documentation (SourceCode.md)

```
These comments will be included in the source code.
Explaining the most complicated parts of the code
    This doesn't necessarily mean 100% commented code
The document will also keep a list of files, line numbers and comments.
Testing criteria: At least 5 items in this list referring to the comments in the complicated parts of your software.
```

In-line Code Documentation
==========================

BudgetCreator.java
------------------

#### Line 78

All of the prerequisite functions must be called before createBudget() is called. A full list of these is

-	setAge
-	setMonthlyIncome
-	setHousingOwnership
-	setHousingPayment
-	setDebt
-	setSavings
-	setLocation

Without calling all of these functions and providing a non-null input, the createBudget() function will fail due to the use of checkNotNull() on all of the provided values from those functions. Without any of these values, the budget cannot be created as it depends on all of them.

#### Line 110, 117, 119

-	50% of income distributed here
-	20% of income distributed here
-	30% of income distributed here

Tracking money as it is sifted into the different parts of the budget is difficult, so these comments simply aim to guide the reader to different portions.

BudgetCategory.java
-------------------

#### Line 29

Burying switch/case setups into enumerations seems to be the healthiest way to do them. This simply links different budget categories to minimum amounts that should be allotted them inside of the budget.
