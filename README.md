sils490-PaleoRecipeBookAPI
==========================
**
Homework Assignment 5: Designing a Hypermedia Type: Paleo Recipe Book; Final**

----------
The following html documents are used to build this project:

list-recipes.ejs, list-ingredients.ejs, one-recipe.ejs, one-ingredient.ejs, index.ejs, app.js

This information (web) service handles Paleo Recipes and Paleo Ingredients ,that are by definition “Paleo”, as its two resources. These recipes do not contain grains, dairy, processed sugar/preservatives, corn or corn byproducts, legumes, or white/starchy potatoes, and only contain fruits, vegetables, meats, and natural sugars. 

Each recipe can be divided into data units made up of the following sections: Recipe Title, Ingredients, Main Ingredient, Prep Instruction, Cooking Instruction, Author Comment, and Comments. These are the components that the service will require information about for each resource.

This API will handle the following representation:

***`1.`	The list of All Recipes by title: /title***

From here the user can navigate to view a single recipe, the list of all recipes, the list of all ingredients, or go back to the home page.

GET returns a list of all recipe Titles. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

POST creates a new recipe. This requires text representations of the Recipe Title, and Id; text representation of Ingredients, Prep Instruction, Cooking Instruction, Main Ingredient, Author Comments, and Comments are optional for this form. If valid, it returns the new objects location: /recipe/{recipe title}. The status code is ‘201 created’ if the request is valid, all necessary data is provided, or ‘400 Bad Request’ if no data or not all data was provided in the request.

***`2.` A sigle recipe identifiable by a recipe Title: /recipe/{recipe title}***

From here the user can navigate to view all the main ingredients associated with this single recipe, the list of all recipes, the list of all ingredients, or go back to the homepage.

GET returns a text representation of the recipe which is specified by the Title. This requires the user to provide a text representation of the Title. If there is no recipe with the specified title, it returns the message: ‘no such recipe’. The status code is ‘200 ok’ if all necessary data is provided.

POST updates or adds comments, ingredients, prep time, or cook instructions, or all the above to the recipe. This requires the user to provide a text representation of each or any of these items. It returns the message: ‘comment added to recipe {title}'.The status code is ‘200 ok’.


***`3.`  The list of All Main Ingredients: /ingredien/{main_ingredient}***

From here the user can navigate to view a single ingredient, the list of all recipes, the list of all ingredients, or go back to the home page.

GET returns a list of all main ingredients without duplicates. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

PUT creates a new ingredient for a recipe. This requires text representations of the ingredient, however, the recipe's ID and Title are dynamically provided by the application. If valid, it returns the new objects location: /ingredietn/{main_ingredient}. The status code is ‘201 created’ if the request is valid, all necessary data is provided, or ‘400 Bad Request’ if no data or not all data was provided in the request.

***`4.` A sigle Main Ingredient identifiable associated with a recipe Title: /ingredient/{main_ingredient}***

From here the user can navigate to view all the recipes titles associated with this single ingredient, the list of all recipes, the list of all ingredients, or go back to the homepage.

GET returns a text representation of the ingredinet which is specified by it's name. This requires the user to provide a text representation of the ingredient. If there is no recipe with the specified title, it returns the message: ‘no such recipe’. The status code is ‘200 ok’ if all necessary data is provided. 

----------

##**Attribut values: id, class, rel, name**


**id attribute values:**

*all-recipes*: 
When used with a div tag specifies a resource that should represent all recipe titles of recipes

*all-ingredients*:
When used with a div tag specifies a resource that should represent all ingredients of recipes

**class attribute values:**

*navigation*:
signifies a link the user can use to navigate across representations

*titles*:
When used with ul tag signifies a list of recipes that can be identified by title

*recipe-text*:
When used with a span tag defines a block of text data that is about a recipe

*all*:
When used with a form tag signifies that this method will search all resources within the representation


*one-recipe*:
When used with ul tag signifies a single recipe

*one-ingredient*:
When used with ul tag signifies a single recipe

**rel attribute values:**

*home-page*:
Refers to a process flow that takes the user to home page.

*all-recipes*:
Refers to a process flow that takes the user to the list of all recipes.

*all-ingredient*:
Refers to a process flow that takes the user to the list of all ingredients


*title*:
When used with an a tag directs the data to refer to a title

*ingredients*:
When used with an a tag directs the data to refer to ingredients

*prep*:
When used with an a tag directs the data to refer to prep instructions

*cooking-instructions*:
When used with an a tag directs the data to refer to cooking instructions

*comments*:
When used with an a tag directs the data to refer to comments

*authors-comments*:
When used with an a tag directs the data to refer to the authors original comments

**name attribut values:**

*all-recipe-titles*:
When used with form signifies a method that returns all recipe titles

*add-recipe*:
When used with form signifies a method that adds a recipe

*title*:
When used with an input tag specifies the the user's input should represent a recipe's title

*add-ingredient*:
When used with an input tag specifies the the user's input should represent a recipe's ingredients

*update-recipe*:
When used with form signifies a method that should update a recipe with comments given as input by the user
