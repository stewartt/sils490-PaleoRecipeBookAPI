sils490-PaleoRecipeBookAPI
==========================
**
Homework Assignment 4: Designing a Hypermedia Type: Paleo Recipe Book**

----------
This information (web) service handles Paleo Recipes that are, by definition “Paleo”, as its primary resources. These recipes do not contain grains, dairy, processed sugar/preservatives, corn or corn byproducts, legumes, or white/starchy potatoes, and only contain fruits, vegetables, meats, and natural sugars. 

Each recipe can be divided into data units made up of the following sections: Recipe Title, Ingredients, Prep Instruction, Cooking Instruction, and Comments. These are the components that the service will require information about for each resource.

This API will handle the following representation:

***`1.`	The list of All Recipes by title: /title***

GET returns a comma separated list of all recipe Titles. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

POST creates a new recipe. This requires text representations of the Recipe Title, Ingredients, Prep Instruction, Cooking Instruction, Category, and Type for the recipe. If valid, it returns the message: ‘new recipe created’ and the new objects location: /recipesearch?recipe_title={recipe title}. The status code is ‘201 created’ if the request is valid, all necessary data is provided, or ‘400 Bad Request’ if no data or not all data was provided in the request.

***`2.` A sigle recipe identifiable by a recipe Title: /{category}/{type}/{title}***

From here the user can navigate to view all titles, all categories, or all types.

GET returns a text representation of the recipe which can be classified by the specified Title. This requires the user to provide a text representation of the Title. If there is no recipe with the specified title, it returns the message: ‘no such recipe’. The status code is ‘200 ok’ if all necessary data is provided.

POST adds comments to the recipe. This requires the user to provide a text representation of the comment.It returns the message: ‘comment added to recipe {title}'.The status code is ‘200 ok’.

DELETE (as a javascript fuction) removes the recipe.This requires the user to provide a text representation of the title of the recipe. If there is no recipe with the specified title, it returns the message: ‘no such recipe’. The status code is ‘200 ok’ if all necessary data is provided.

***`3.` A list of all recipe categories the API knows, based on the resources it knows. /category***

From here the user can navigate to view all titles or all types

GET returns a comma separated list of all recipe categories. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

***`4.` A list of all recipe types the API knows, based on the resources it knows. /type***

From here the user can navigate to view all titles or all categories

GET returns a comma separated list of all recipe types. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

***`5.` A query for a specific recipe. /title***

GET returns a comma separated list of all recipe types. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

----------

##**Attribut values: id, class, rel, name**


**id attribute values:**

*all-recipes*: 
When used with a div tag specifies a resource that should represent all recipe titles of recipes

*all-categories*:
When used with a div tag specifies a resource that should represent all categories of recipes

*all-types*:
When used with a div tag specifies a resource that should represent all types of recipes

*recipe*:
When used with a div tag specifies a resource that should represent a single recipe

*find-recipes*:
When used with a div tag specifies a resource that should represent a query for a recipe

**class attribute values:**

*navigation*:
signifies a link the user can use to navigate across representations

*titles*:
When used with ul tag signifies a list of recipes that can be identified by title

*recipe-text*:
When used with a span tag defines a block of text data that is about a recipe

*all*:
When used with a form tag signifies that this method will search all resources within the representation

*categories*:
When used with ul tag signifies a list of recipe categories

*category-text*:
When used with a span tag defines a block of text data that is about a recipe category

*types*:
When used with ul tag signifies a list of recipe types

*type-text*:
When used with a span tag defines a block of text data that is about a recipe type

*single*:
When used with ul tag signifies a single recipe

*single*:
When used with a form tag signifies that this method will search for and return only one resource representation


**rel attribute values:**

*category-page*:
Refers to a process flow that takes the user to the category page, which can list the categories

*type-page*:
Refers to a process flow that takes the user to the type page, which can list the types

*title-page*:
Refers to a process flow that takes the user to the title page, which can list all titles

*category*:
When used with an a tag directs the data to refer to a category

*type*:
When used with an a tag directs the data to refer to a type

*title*:
When used with an a tag directs the data to refer to a title

*ingredients*:
When used with an a tag directs the data to refer to ingredients

*prep-instructions*:
When used with an a tag directs the data to refer to prep instructions

*cooking-instructions*:
When used with an a tag directs the data to refer to cooking instructions

*comments*:
When used with an a tag directs the data to refer to comments

**name attribut values:**

*all-recipe-titles*:
When used with form signifies a method that returns all recipe titles

*add-recipe*:
When used with form signifies a method that adds a recipe

*title*:
When used with an input tag specifies the the user's input should represent a recipe's title

*ingredients*:
When used with an input tag specifies the the user's input should represent a recipe's ingredients

*prep instructions*:
When used with an input tag specifies the the user's input should represent a recipe's prep instructions

*cooking instructions*:
When used with in input tag specifies the the user's input should represent a recipe's cooking instructions

*category*:
When used with an input tag specifies the the user's input should represent a recipe's category

*type*:
When used with an input tag specifies the the user's input should represent a recipe's type

*all-recipe-categories*:
When used with form signifies a method that should return all categories of recipes

*all-recipe-types*:
When used with form signifies a method that should return all types of recipes

*add-comment*:
When used with form signifies a method that should update a recipe with comments given as input by the user

*comment*:
When used with an textarea tag specifies the the user's text should be appropriate for a comment field

*search-title*:
When used with form signifies a method that should search for a recipe by a given title
