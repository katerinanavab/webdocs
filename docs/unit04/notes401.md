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

{:.highlight}
The `<script>` tag contains JavaScript code which is **automatically executed** when the browser processes the tag. If we have a lot of JavaScript code, we can put it into a **separate file**, like the `script.js` file already in your project repository.

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

The first thing we'll study is the **building blocks** of JavaScript code.

<html>
<dl>
<dt>Syntax</dt>
<dd>The "grammar" rules of a programming language, which include meaningful <strong>symbols</strong>, <strong>keywords</strong>, and <strong>patterns</strong>.</dd>
<dt>Statements</dt>
<dd>Statements are <strong>syntax constructs</strong> and <strong>commands</strong> that perform <em>actions</em>.</dd>
</dl>
</html>

We've already seen a _statement_, `console.log('Hello world!');`, which shows the message "Hello, world!" in the **OUTPUT** frame.

{:.highlight}
We can include as many **statements** (commands/instructions) in our code as we want! Statements are separated with a _semicolon_ (` ; `).

#### Comments
{:.no_toc}

As time goes on, programs become more and more complex. It becomes necessary to add *comments* which describe what the code does and why.

Comments can be put into any place of a script. They don't affect its execution because the engine simply **ignores** them.

{:.important}
**One-line comments start with two forward slash characters `//`.**

The rest of the line is a comment. It may occupy a full line of its own or follow a statement.

Like here:
```js
// This comment occupies a line of its own
alert('Hello');

alert('World'); // This comment follows the statement
```

{:.important}
**Multiline comments** start with a forward slash and an asterisk <code>/&#42;</code> and end with an asterisk and a forward slash <code>&#42;/</code>.

Like this:
```js
/* An example with two messages.
This is a multiline comment.
*/
alert('Hello');
alert('World');
```

The content of comments is **ignored**, so if we put code inside <code>/&#42; ... &#42;/</code>, it won't execute.

Sometimes it can be handy to _temporarily disable_ a part of code:

```js
/* Commenting out the code
alert('Hello');
*/
alert('World');
```


### Variables & Data Types

<iframe width="560" height="315" src="https://www.youtube.com/embed/cXUWYZXru6o?si=sB54GV-STb2ipVhL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Most of the time, a JavaScript application needs to work with information. Here are two examples:
1. An online shop -- the information might include goods being sold and a shopping cart.
2. A chat application -- the information might include users, messages, and much more.

Variables are used to store this information.

A [variable](https://en.wikipedia.org/wiki/Variable_(computer_science)) is a "named storage" for data. We can use variables to store goodies, visitors, and other data.

To create a variable in JavaScript, use the `let` keyword.

The statement below creates (in other words: *declares*) a variable with the name "message":

```js
let message;
```

Now, we can put some data into it by using the assignment operator `=`:

```js
let message;

*!*
message = 'Hello'; // store the string 'Hello' in the variable named message
*/!*
```

The string is now saved into the memory area associated with the variable. We can access it using the variable name:

```js
let message;
message = 'Hello!';

*!*
alert(message); // shows the variable content
*/!*
```

To be concise, we can combine the variable declaration and assignment into a single line:

```js
let message = 'Hello!'; // define the variable and assign the value

alert(message); // Hello!
```

#### `var` instead of `let`
{:.no_toc}

In older scripts, you may also find another keyword: `var` instead of `let`:

```js
var message = 'Hello';
```

The `var` keyword is *almost* the same as `let`. It also declares a variable but in a slightly different, "old-school" way.

There are subtle differences between `let` and `var`, but they do not matter to us yet. 


#### A real-life analogy
{:.no_toc}

We can easily grasp the concept of a "variable" if we imagine it as a "box" for data, with a uniquely-named sticker on it.

For instance, the variable `message` can be imagined as a box labelled `"message"` with the value `"Hello!"` in it:

![image](variable.svg)

We can put any value in the box.

We can also change it as many times as we want:

```js run
let message;

message = 'Hello!';

message = 'World!'; // value changed

alert(message);
```

When the value is changed, the old data is removed from the variable:

![image](variable-change.svg)

We can also declare two variables and copy data from one into the other.

```js
let hello = 'Hello world!';

let message;

// copy 'Hello world' from hello into message
message = hello;

// now two variables hold the same data
alert(hello); // Hello world!
alert(message); // Hello world!
```

<div class="warn" markdown="block">

A variable should be **DECLARED** only once. A repeated declaration of the same variable triggers an error:

```js run
let message = "This";

// repeated 'let' leads to an error
let message = "That"; // SyntaxError: 'message' has already been declared
```
So, we should declare a variable once and then refer to it without `let`.

</div>

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
