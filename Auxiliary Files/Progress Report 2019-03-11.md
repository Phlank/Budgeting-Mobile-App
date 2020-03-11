Progress Report
===============

2019-03-11

Iteration 4 Conclusion
----------------------

-	Bug fixes nearly finished

Iteration 5 Roadmap
-------------------

### High level features

#### Account interfaces

Colin is doing research into what typical account integration service involves. If there are any pointers of connections to existing Accutech staff to understand requirements for this piece of software, direction would be very appreciated.

#### Gamification

All gamification must center around the concept that we are making an app that helps people organize their lives now so their future can be greater than they thought possible.

-	Achievements
	-	Weekly spending
	-	Monthly spending
	-	Spending challenges
		-	If user can cut down on low-priority spending, offer more rewards
		-	"You've been spending X on Y. If you can manage to spend N less on Y, you can finally get Z."
-	Rewards
	-	What is user saving for?
	-	What is user working towards? (Saving goals like 1, 2, and 3 months of income saved would be awesome starting goals)
	-	**Bryan**, could you think of other goals similar to the one above that are related to basic self-reliance and money management?
-	Help users achieve goals with specific direction.

#### Asset valuation

-	Car value
-	Home value
-	Connect with outside resources e.g. Kelly Blue Book, Zillow, etc.
-	How to display these values? Where to put them?

### Low level features

#### Persistence

App currently stores all information into encrypted files, might be worth switching to database over a weekend off work. - Advantages: Easier data management - Disadvantages: SQLite and SQLCipher libraries are quite young in Flutter and may change before the first major release, time could be spent on other things.

#### Documentation

Start documenting key aspects of the software and how they work together. Since this is a from-scratch project, we need to be thorough in our explanations of how things work and why we decided they should work that way.
