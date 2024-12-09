---
layout: project
title: "💻PROJECT #2.3"
projectname: "CSS Movie Scene"
parent: "2️⃣ Advanced CSS"
nav_order: 7
---


### Overview & Setup


> 🧠 **BRAINSTORM:** Pick your favorite movie! 

<div class="setup" markdown="block">

1. Go to the `CS1 Project 2.3` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Project 2.3` assignment on Blackbaud.

</div>

--- 

### Instructions

#### Part A: Setting Up the Starter Code

<div class="task" markdown="block">
  
1. Add Starter CSS Code
  * Write the following style rules in `style.css`:
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html, body {
  height: 100%;
  width: 100%;
}
```
2. Set the Background
  * Add a `body` style to include a background image:
```css
body {
  background-image: url("https://wallpaper.dog/large/20552168.jpg");
  background-size: cover;
}
```
3. Add the Scene Description Section
  * Inside the `<body>` tag in `index.html`, create a container to describe the scene:
```html
<div id="scene-description">
  <h1>Scene Title</h1>
  <p>Scene Description</p>
</div>
```
  * Update the CSS to style it:
```css
#scene-description {
  width: 600px;
  margin: 20px auto;
  text-align: center;
  font-family: "Trebuchet MS", Sans-Serif;
  font-size: 0.8em;
  color: white;
}
```
4. Add the Scene Container
  * Below the `#scene-description`, add the main animation space:
```html
<div id="scene-container"></div>
```
  * Style it in CSS:
```css
#scene-container {
  width: 600px;
  height: 400px;
  margin: auto;
  border: 5px solid black;
  background-color: white;
  overflow: hidden;
}
```
5. Test Your Page
  * _You should see:_
    * A background image covering the whole page.
    * A centered description section with text.
    * A bordered white box ( `#scene-container`) for your scene.

</div>

#### Part B: 

<div class="task" markdown="block">

</div> 

--- 

### Minimum Requirement Checklist

- _HTML Content:_
  - [ ] Include at least **6 HTML elements** inside the `#scene-container` with distinct classes or ids, using the appropriate tags (e.g., `<div>`, `<p>`, `<span>`, `<img>`).
- _CSS Base Styles:_
  - [ ] Style all elements to fit your **theme** (e.g., colors, sizes, positioning).
- _CSS Animations:_
  - [ ] Define at least 2 distinct `@keyframes` **animation sequences**. One of these must have _more than 2 points_ in the animation sequence (e.g. `0%`, `50%`, `100%` rather than just `from` and `to`).
  - [ ] In a selector for the **element** to be animated, specify the relevant **animation** **properties** (e.g., `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`).
- _CSS Transforms:_
  - [ ] Apply at least 4 different `transform` functions (e.g., `rotate`, `scale`, `translate`).
- _CSS Positioning:_
  - [ ] Use at least 2 different **positioning techniques** (e.g., `absolute`, `relative`, or `fixed`).
- _CSS Customization:_
  - [ ] Adjust the `background` of the movie scene, or `border` styles for visual appeal.
  - [ ] Ensure that the final product of your movie scene looks **cohesive**.

#### Bonus Features
- Include an **interactive** effect (e.g., `:hover` selector with a `transition` property).
- Use CSS **variables** for repeated values.
- Create a "start" `button` that triggers animations using a class toggle (simple `JavaScript`).
- Experiment with CSS `clip-path` or `filter` for advanced effects.

{:.highlight}
**RESOURCES:** While working on this project or attempting the bonus features, you are encouraged to look up any CSS `properties` on Google or [📖 W3Schools](https://www.w3schools.com/css/), review our [📓 Unit 1 Notes](https://coderina.dev/webdocs/unit01) or [📓 Unit 2 Notes](https://coderina.dev/webdocs/unit02), and make use of the helpful [🎨 SheCodes CSS Tools](https://generators.shecodes.io/). 


