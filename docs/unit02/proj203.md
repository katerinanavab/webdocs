---
layout: project
title: "💻PROJECT #2.3"
projectname: "CSS Movie Scene"
parent: "2️⃣ Advanced CSS"
nav_order: 7
---


### Overview & Setup

CSS **animations** and **transforms** are powerful tools that bring life to web pages. With **animations**, we can create smooth transitions, moving objects, or even complex _sequences_ of changes, making websites more interactive and visually appealing. **Transforms** allow us to _manipulate elements_ by rotating, scaling, or repositioning them, enabling unique and dynamic designs.

In this project, you'll practice these techniques by building an **animated scene** inside a defined container. You’ll experiment with movement, resizing, and interactivity to make a creative and engaging display. 

> 🧠 **BRAINSTORM:** Look up on Google Images: _"iconic scenes from..."_ + the title of your favorite **movie**, **show**, or **book**. 

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
  
1. **Add Starter CSS Code**
    * Write the following style rules in `style.css`:
```css
html, body {
    height: 100%;
    width: 100%;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
2. **Set the Background**
    * Add a `body` style rule to include a background image:
```css
body {
    background-image: url("https://wallpaper.dog/large/20552168.jpg");
    background-size: cover;
}
```
3. **Add the Scene Description Section**
    * Inside the `<body>` tag in `index.html`, create a container to describe the scene: `<div id="scene-description"></div>`
    * Inside that `<div>`, include an `<h1>` element with the scene **title** and a `<p>` element with a brief **description** of the scene. 
```
4. **Style the Scene Description**
    * In `style.css`:
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
5. **Add the Scene Container Section**
    * Below the `#scene-description`, add the main animation space:
```html
    <div id="scene-container"></div>
```
6. **Style the Scene Container**
    * In `style.css`:
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

</div>

#### Part B: Adding Animations and Transforms

<div class="task" markdown="block">

1. Plan your Scene
    * Pick an **iconic scene** from a movie, TV show, or book that you'd like to model.
    * Identify several possible animations to make your scene dynamic (e.g., a bouncing ball, flying objects, spinning elements, people walking, etc.).
2. Add Elements to the Scene
    * Inside the #scene-container, add HTML elements to animate. For example:
```html
<div id="ground"></div>
<span id="football">🏈</span>
<img id="actor" src="">
````
3. Style the Elements
    * Define styles for the new elements in the style.css file or within the <style> tag. Example:
css
Copy code
.object {
    width: 50px;
    height: 50px;
    background-color: red;
    border-radius: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
4. Add CSS Animations

Use the @keyframes rule to define animations. Example:
css
Copy code
@keyframes bounce {
    0%, 100% {
        top: 50%;
    }
    50% {
        top: 10%;
    }
}

.object {
    animation: bounce 2s infinite;
}
5. Experiment with Transforms

Use transform properties like rotate, scale, and translate to enhance animations:
css
Copy code
.object {
    transform: scale(1);
    animation: bounce 2s infinite, spin 4s linear infinite;
}

@keyframes spin {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

6. Test and Adjust
    * Ensure the animations are smooth and work well together. Adjust durations, delays, and easing functions as needed.

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
- Include an **interactive** effect (e.g., `:hover` pseudo-class selector with a `transition` property).
  - See [W3Schools - Transitions](https://www.w3schools.com/css/css3_transitions.asp) and [W3Schools - Pseudoclasses](https://www.w3schools.com/css/css_pseudo_classes.asp)
- Use CSS **variables** for repeated values.
  - See [W3Schools - Variables](https://www.w3schools.com/css/css3_variables.asp) 
- Create a "start" `button` that triggers animations using a class toggle (requires some `JavaScript`).
- Experiment with CSS `clip-path` or `filter` for advanced effects.

{:.highlight}
**RESOURCES:** While working on this project or attempting the bonus features, you are encouraged to look up any CSS `properties` on Google or [📖 W3Schools](https://www.w3schools.com/css/), review our [📓 Unit 1 Notes](https://coderina.dev/webdocs/unit01) or [📓 Unit 2 Notes](https://coderina.dev/webdocs/unit02), and make use of the helpful [🎨 SheCodes CSS Tools](https://generators.shecodes.io/). 


