---
layout: notes
title: "📓NOTES 4.1: JavaScript Programming" 
parent: "4️⃣ JavaScript"
nav_order: 1
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---
#### New Unit! Use a GitHub Template for class notes:
{:.no_toc}

<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Unit-4-Notes` or `CS1-JavaScript-Notes`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Take notes in this Codespace during class, coding along with the instructor.

</div>

---

## Introduction to Programming in JavaScript (JS)

*JavaScript* was initially created to "make web pages alive"!

{:.highlight}
📝 The programs coded in this language are called *scripts*. They can be written right in a web page's HTML and are run **automatically** as the page loads.

> **NOTE:** In this aspect, JavaScript is very different from another language called [Java](https://en.wikipedia.org/wiki/Java_(programming_language)). When JavaScript was created, it initially had another name: "LiveScript". Java was very popular at that time, so it was decided that positioning a new language as a "younger brother" of Java would help.

Today, JavaScript can execute not only in the **browser**, but also on the server, or actually on any device that has a special program called [the JavaScript engine](https://en.wikipedia.org/wiki/JavaScript_engine). The browser has an embedded engine sometimes called a "JavaScript virtual machine".

### What can in-browser JavaScript do?
{:.no_toc}

🌐 _In-browser_ JavaScript can do everything related to **webpage manipulation** as well as **interaction** with the user and the webserver.

For instance, in-browser JavaScript is able to:

- ⭐️ Add **new HTML** to the page, **change** the existing content, **modify CSS** styles.
- ⭐️ React to user **actions**, like mouse clicks, pointer movements, key presses.
- ⭐️ Ask **questions** to the visitor, **display** messages and alerts.
- Remember the data on the client-side ("local storage").
- Send requests over the network to remote servers, download and upload files (so-called [AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) and [COMET](https://en.wikipedia.org/wiki/Comet_(programming)) technologies).

### The script tag
{:.no_toc}

JavaScript programs can be inserted almost anywhere into an HTML document using the `<script>` tag: 

```html
<body>

  <p>Before the script...</p>

  <script>
    console.log('Hello, world!');
  </script>

  <p>...After the script.</p>

</body>
```

▶️ The `<script>` tag contains JavaScript code which is **automatically executed** when the browser processes the tag.

{:.highlight}
If we have a lot of JavaScript code, we can put it into a **separate file**, like the `script.js` file already in your project repository.

Script files are attached to HTML with the `src` **attribute**:

```html
<script src="/path/to/script.js"></script>
```

> Here, `/path/to/script.js` is an **absolute path** to the script from the site root. One can also provide a **relative path** from the current page. For instance, `src="script.js"`, just like `src="./script.js"`, would mean a file `"script.js"` in the current folder.

We can give a **full URL** as well. For instance:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/lodash.js/4.17.11/lodash.js"></script>
```

To attach **several scripts**, use multiple tags:

```html
<script src="/js/script1.js"></script>
<script src="/js/script2.js"></script>
…
```

{:.highlight}
As a rule, only the simplest scripts are put _directly_ into HTML. More complex ones reside in **separate files**. The benefit of a separate file is that **the browser will download it** and store it in its [cache](https://en.wikipedia.org/wiki/Web_cache). 
> Other pages that reference the same script will take it from the cache instead of downloading it, so the file is actually downloaded only _once_. That reduces traffic and makes pages faster!

### JS Code Structure

<html>
<dl>
<dt>Syntax</dt>
<dd>The "grammar" rules of a programming language, which include meaningful <strong>symbols</strong>, <strong>keywords</strong>, and <strong>patterns</strong>.</dd>
<dt>Statements</dt>
<dd>Statements are <strong>syntax constructs</strong> and <strong>commands</strong> that perform <em>actions</em>.</dd>
</dl>
</html>



### Variables & Data Types

<iframe width="560" height="315" src="https://www.youtube.com/embed/cXUWYZXru6o?si=sB54GV-STb2ipVhL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

<div class="task" markdown="block">

Complete **steps 1-6** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

### Operators & Logic

<div class="task" markdown="block">

Complete **steps 7-9** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

### Conditional Branching (`if`)

<div class="task" markdown="block">

Complete **steps 10-14** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

### Iteration/Loops (`while`, `for`)

<!--

### Using Methods

<div class="task" markdown="block">

Complete **steps 15-20** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

### Writing Functions

<div class="task" markdown="block">

Complete **steps 21-?** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

-->

---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide), [The Modern JavaScript Tutorial](https://javascript.info/), and [CodeAnalogies Blog](https://www.codeanalogies.com/).
{: .fs-2 }
