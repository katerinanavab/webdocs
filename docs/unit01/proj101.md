---
layout: project
title: "💻PROJECT #1.1"
projectname: "Recipe Website"
parent: "1️⃣ Web Dev Foundations"
nav_order: 5
---

### Overview & Setup

It's time to practice all of the HTML knowledge you have acquired. In this project, you are going to build a basic recipe website.

The website will consist of a main index page which will have links to a few recipes. The website won't look very pretty by the time you've finished, unless you're into [brutalist web design](https://brutalistwebsites.com/), that is.

But it's important to keep in mind that this project is just to build your HTML chops; we will revisit this project in the future to style it up with CSS.

<div class="setup" markdown="block">

1. Go to the `CS1 Project 1.1` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Project 1.1` assignment on Blackbaud.

</div>

### Instructions & Requirements

#### Iteration 1: Create Initial Structure
<div class="task" markdown="block">

1. Within the project, navigate to the `index.html` file.
1. Ensure that it is already filled out with the usual **boilerplate HTML**.
2. Add an `h1` heading in the body section that describes the main title of the website (like _"My Favorite Recipes"_ or _"Sweet Treats for Fall"_).

</div> 

#### Iteration 2: Start Recipe Page

<div class="task" markdown="block">
 
1. Create a **new directory (folder)** within the project and name it `recipes`.
1. Create a **new HTML file** within the  `recipes` directory and name it after the recipe it will contain.
> For example `lasagna.html`. You can use the name of your favorite dish or, if you need some inspiration, you can find a recipe to use at [Allrecipes](https://www.allrecipes.com/).
1. For now, just include an `h1` **heading** with the recipe's name as its content.
1. Back in the `index.html` file, add a **link** to the recipe page you just created.

_Example:_ Under the `<h1>My Recipes</h1>` heading, write out the link like so: `<a href="recipes/recipename.html">Recipe Title</a>`. The text of the link should again be replaced with the actual recipe name.

</div>

#### Iteration 3: Add Recipe Page Content

<div class="task" markdown="block">
 
Your new recipe page must have the following content:
1. An **image** of the finished dish under the h1 heading that you added earlier. You can find images of the dish on Google or [Allrecipes](https://www.allrecipes.com/).
1. Under the image, it should have an appropriately sized "Description" **heading** followed by a **paragraph** or two describing the recipe.
1. Under the description, add an "Ingredients" heading followed by an **unordered list** of the ingredients needed for the recipe.
1. Finally, under the ingredients list, add a "Steps" heading followed by an **ordered list** of the steps needed for making the dish.

</div>

#### Iteration 4: Add More Recipes

<div class="task" markdown="block">

1. Add **two more recipes** with identical page structures to the recipe page you've already created.
1. Don't forget to **link** to the new recipes on the index page. Also, consider putting all the links in an unordered list so they aren't all on one line.

_Example:_

```html
 <ul>
    <li><a href="recipes/yourrecipe.html">Recipe Title 1</a></li>
    <li><a href="recipes/yourrecipe.html">Recipe Title 2</a></li>
    <li><a href="recipes/yourrecipe.html">Recipe Title 3</a></li>
  </ul>
```
  
Your links won't be flashy, but for now, just focus on building them out.

</div>


---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [The Odin Project](https://www.theodinproject.com/).
{: .fs-2 }
