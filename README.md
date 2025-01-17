# Order Up

This repository requires and has been tested on Ruby v2.5.3 and is based on Rails 5.2.4.3.

RSpec and Shoulda-Matchers have been installed and set up.

## Setup

1. fork this repo
2. clone your fork
3. `git clone <paste_repo>`
4. `cd b2-mid-mod`
5. `bundle install`


## Overview

Order up is an app that tracks chefs, the dishes that they make, and the ingredients that are in those dishes.

* Chef's have many dishes
* Dishes belong to a chef
* Dishes have many Ingredients
* Ingredients have many dishes
* Ingredients should have a name and calories.

Some of the initial migrations and model set up has been done for you. After you set up your database, you should be able to run the tests and see five passing tests.

(Note: The plural of dish is dishes. The plural of chef is chefs.)

## User Stories

```
User Story 1 - Ingredient Show Page (features)

As a visitor
When I visit an ingredient's show page
Then I see the name and calories of the ingredient
And I see the names and descriptions of all dishes that include this ingredient
```

```
User Story 2 - Ingredient's Chefs  (active record)

As a visitor
When I visit an ingredient's show page
Then I see the name of all chefs that use this ingredient in any of their dishes
And I see that the list of chefs is unique (contains no duplicate chefs)
And I see that the chefs are ordered alphabetically by name (A - Z)
```

```
User Story 3 - Remove a Dish from the Ingredient (focused on a delete route, dish ingredients controller that deletes relationship between dish and ingredient)

As a visitor
When I visit an ingredient's show page
Then next to each dish I see a button to remove it
When I click one of these buttons
Then the ingredient is no longer associated with the dish
And I am returned to the ingredient's show page
And I no longer see the dish listed 
(Note: You should not destroy the dish record entirely)
```


## Extensions

```
Extension - Chef's most popular ingredients

As a visitor
When I visit a chef's show page
I see a section for "Most Popular Ingredients"
And in that section I see the three most popular ingredients that the chef uses in their dishes
(Note: Popularity is based off of how many dishes use that ingredient)
(Note: You should only make 1 database query to calculate the most popular ingredients)
```
