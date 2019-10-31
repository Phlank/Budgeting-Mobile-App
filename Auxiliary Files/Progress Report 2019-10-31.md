Progress Report - Budgeting Mobile App
======================================

10-31-2019

Research
--------

We've done research mostly on mobile apps and their design, but not very much on the side of automatically generating budgets from a few variables. This is something with a lot of "hidden magic" behind it - we have to be able to make a lot of assumptions about our users.

Because of these considerations, we've begun to organize different "budget sections" into various priorities. Things like rent or house payments should be considered non-negotiable, as should food and utilities. However, finding a proper amount to assume for some of these is more difficult.

Budget Sections
---------------

-	Home
-	Utilities
-	Groceries
-	Savings
-	Health
-	Transportation
-	Education
-	Entertainment
-	Kids
-	Pets
-	Miscellaneous

The sorting of these items is not cut-and-dry for each person, but an overall designation can be made.

#### Non-negotiables

The items that must come before all else. None of these items can be shortchanged for a month without severe loss of quality of life.

1.	Home (rent and house payments)
2.	Utilities
3.	Groceries

#### High priority

Without these, quality of life diminishes significantly, but it is much easier to come back from this than not being able to provide the non-negotiables. These items can have a direct impact on income.

1.	Health
2.	Transportation
3.	Education
4.	Savings

#### Low priority

These impact long-term quality of life as opposed to day-to-day quality of life. Without any entertainment or miscellaneous spending, life will seem less passionate and this can lead ultimately to a lack of drive.

1.	Entertainment
2.	Pets
3.	Miscellaneous

The challenge
-------------

Our design centers around the basic information provided by the user of:

-	Age
-	Income
-	Renting or owning, payment amount
-	Total debt
-	Size of savings account

A lot of this type of extrapolation is beyond our expertise, and we need some guidance here. There are a few different methods that we've thought of, but we're not sure which route to take.

#### Method #1 - Minimum + scaling

The idea behind this method is that each budget section has a minimum amount to spend per month, and that is as low as our app will go (yes, zero is an option here). Then based on income, each section slowly scales up. This could also be useful to adjust the weighting of different things; suppose someone wants to save more than someone else - they could simply adjust the weight of their budget towards savings as opposed to lower priority options.

#### Method #2 - Average consumer data for location

It may be average in Indiana that people spend $150 on groceries per person in their home. So, that would be our baseline for a category. However, this isn't the most *thrifty* option we can imagine, but it's based on something more real for an area someone lives in than just a random minimum number. Finding data about this sort of thing would be difficult, and we'd have to stay updated on many regions in order to make this work. However, this may provide really good results.

#### Method #3 - Purchase tracking

This goes beyond the initial expectations of the software, but it's still an option. There are a lot of tools out there that can take a picture of a receipt and sort the purchases into sections or dump it all into one section. This might be better for refining the budget, but if we want a budget from the get-go which we see happening, then this isn't the way to start.

This is where we need some more from you...
-------------------------------------------

We're not sure exactly which direction to take this in. Maybe you have some more ideas about how this could work. Perhaps we need to do some more thinking on the budget sections moving forward, or maybe that's a good start and we should see what we can come up with for it so far. Essentially, we've identified a lot of possible paths, and we need help determining which one is worth risking our time.

Thank you for your help with this!
