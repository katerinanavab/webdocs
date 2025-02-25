---
layout: notes
title: "📓NOTES 4.3: Conditionals & Iteration" 
parent: "4️⃣ JavaScript"
nav_order: 3
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---

## Program Flow Control

---

## Branching (Conditionals)

### `if` Statements

<div class="task" markdown="block">

Complete **steps 7-14** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

### Comparison Operators

### "Truthiness"

When we use `if()` statements, we are not always going to be able to plug in a variable with a value of true or false. Many times, we must plug in a **statement** that will be _evaluated_ by JavaScript as `true` or `false`.

> This is similar to the legal system! Although it is POSSIBLE that there will be one piece of evidence that makes the “guilty” or “not guilty” sentence obvious, it is also likely that a judge or jury will need to evaluate the evidence and make a decision.

For this analogy, let's assume a `true` statement is one that will lead to the conviction of the accused car theft, while a `false` statement will let him/her walk free. Let’s create a variable called `evidence` and set it to `true`: 

```js
let evidence = true;
 
if (evidence) {
  convict();
}
 
else {
  release();
}
```
> `convict()` and `release()` are made-up functions. In this case, since evidence is set to true, the judge would convict the car thief. 

Here’s an interactive diagram of this scenario:

<iframe src="https://blog.codeanalogies.com/wp-admin/admin-ajax.php?action=h5p_embed&id=19" width="680" height="322" frameborder="0" allowfullscreen="allowfullscreen" title="True Value in If Statement"></iframe><script src="https://blog.codeanalogies.com/wp-content/plugins/h5p/h5p-php-library/js/h5p-resizer.js" charset="UTF-8"></script>

---

## Looping (Iteration)

### `while` Loops 

### `for...in` loops


---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide), [The Modern JavaScript Tutorial](https://javascript.info/), and [CodeAnalogies Blog](https://www.codeanalogies.com/).
{: .fs-2 }
