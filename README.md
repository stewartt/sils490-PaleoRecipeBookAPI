sils490-PaleoRecipeBookAPI
==========================
**
Homework Assignment 4: Designing a Hypermedia Type: Paleo Recipe Book**

----------
This information (web) service handles Paleo Recipes that are, by definition “Paleo”, as its primary resources. These recipes do not contain grains, dairy, processed sugar/preservatives, corn or corn byproducts, legumes, or white/starchy potatoes, and only contain fruits, vegetables, meats, and natural sugars. 

Each recipe can be divided into data units made up of the following sections: Recipe Title, Ingredients, Prep Instruction, Cooking Instruction, and Comments. These are the components that the service will require information about for each resource.

This API will handle the following for the user:

`1.`	The list of All Recipe Titles: /title

GET  returns a comma separated list of all recipe Titles. Requires no representations from the user. If there are no recipes, it returns the message:’ no recipes have been created.’.The status code is 200 ok. 

POST creates a new recipe. This requires text representations of the Recipe Title, Ingredients, Prep Instruction, Cooking Instruction, Category, and Type for the recipe. If valid, it returns the message: ‘new recipe created’ and the new objects location: /recipesearch?recipe_title={recipe title}. The status code is ‘201 created’ if the request is valid, all necessary data is provided, or ‘400 Bad Request’ if no data or not all data was provided in the request.

`2.` A recipe identified by a recipe Title: /recipesearch?recipe_title={recipe title}

GET returns a text representation of the recipe which can be classified by the specified Title. This requires the user to provide a text representation of the Title. If there is no recipe with the specified title, it returns the message: ‘no such recipe’. The status code is ‘200 ok’ if all necessary data is provided, or ‘400 Bad Request’ if no data or not all data was provided in the request.

PUT replaces/update/add comments to some contents of the recipe. This requires the user to provide a text representation of the comment.It returns the message: ‘comment added to recipe {title}'.The status code is ‘200 ok’.

DELETE removes the recipe.This requires the user to provide a text representation of the title of the recipe. If there is no recipe with the specified title, it returns the message: ‘no such recipe’. The status code is ‘200 ok’ if all necessary data is provided.



----------

##**Attribut values: id, class, rel, name**

**id attribute values:**


**class attribute values:**


**rel attribute values:**


**name attribut values:**

 