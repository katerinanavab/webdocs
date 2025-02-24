---
layout: notes
title: "📓NOTES 4.2: Variables & Functions" 
parent: "4️⃣ JavaScript"
nav_order: 2
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---

## Variables & Data Types

Most of the time, a JavaScript application needs to work with **data** (information). Here are two examples:
1. An online shop - the information might include goods being sold and a shopping cart.
2. A chat application - the information might include users, messages, and much more.

**Variables** are used to _store_ information. A [variable](https://en.wikipedia.org/wiki/Variable_(computer_science)) is a "named storage" for data. We can use variables to store goodies, visitors, and other data.

<div class="imp" markdown="block">

##### Key points:
{:.no_toc}

- **DATA** is information 🧠
- **VARIABLES** store data → *like a **box** * 📦
- **DATA TYPES** are categories of data → *like **labels** on the boxes* 🏷️
    
</div>

#### JS DATA TYPES
{:.no_toc}

| `Number` | 🔢 a **quantity/amount** that is either a **whole/integer** number or a **decimal/fractional** number |
| `String` | 🔤 a collection of **individual characters** (letters/numbers/symbols) that are “*strung together*” to form **text/words/sentences** |
| `Boolean` | either `true` or `false` |
| `Array` | a **list** of multiple values, each value has an **index** number that indicates its position/order in the collection  |
| `Object` | *custom* data types that hold a **group** of data, usually to represent a real-world object or an HTML document |

#### Creating Variables
{:no_toc}

<iframe width="560" height="315" src="https://www.youtube.com/embed/cXUWYZXru6o?si=sB54GV-STb2ipVhL" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

To create a variable in JavaScript, use the `let` keyword.

- **VARIABLES** are containers for *carrying values* within your script

![image](truck-declare-var.gif)

- This is called **declaring** a variable. It creates a new truck called *days* that can drive around your script and deliver its **value** OR pick up a new **value**.
- The `let` **KEYWORD (also** `var` but no one uses that anymore**)** allows us to create **mutable** variables whose values can be changed.
    - `let` announces that you are creating a new variable. Or, in the analogy we are about to use, buying a new truck.
    - If we used the `const` keyword, it would mean that the value is **immutable** and unchangeable.
- The variable needs a unique **name**, which is *days* here. This distinguishes this truck from all the other trucks.
- The **assignment operator**, or `=` sign, is NOT an “equals sign” like in math equations → it’s more like **a ramp that loads up a truck**
    - In this example, it loads the **value** 7, into the *days* truck
- The variable `days` is not “equal” to anything! It merely carries around the value that you assign to it.
- In JS, unlike math, you can simply **RE-ASSIGN** a new value to the variable later: `days = 5;` → the assignment operator loads a new value on to the *days* truck
- You can **PASS** a variable into **FUNCTIONS** like this:
    
![image](truck-use-var.gif)

   
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

```js
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

```js
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

### Arithmetic Operators & Logic

<div class="task" markdown="block">

Complete **steps 7-9** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

---

## Functions

<div class="imp" markdown="block">
    
- **FUNCTIONS** are **reusable** sets of **code** **statements** that accomplish a specific task in a certain way
    - `console.log()` is a built-in **function** that **prints** data by *logging* information in the console
    - Inside the **parenthesis** (`()`) goes the data to be printed
    - Indicate `String` data by surrounding it with **quotations** (`””`) → 💬

</div>

```jsx
// Print a String to the console
console.log("Hello World!");
```

Let's think about the general concept of **cooking with a recipe** first. Using a recipe means that:

1. You start with a specific set of ingredients
2. You perform a specific procedure using those ingredients
3. You will get a reliable product at the end

- A **FUNCTION** is also a **reusable recipe** that performs the same set of actions over and over again on a set of ingredients.
- Those **ingredients** are called **PARAMETERS → “INPUT”**
- Some functions **RETURN** a value, which means that they ***give you a new value*** that you can then use throughout your script **→** “**OUTPUT”**

![image](function-void.png)

- Other functions **do not return** a value, instead, they might ***change a value that already exists*** in your script or carry out an action like `console.log()`
    - Think of it like chopping onions. There is no "new" product, just the same product in a new format.
    - Boiling water to make pasta is another example of a function that just “does/changes something” but doesn’t necessarily give you something new in return
    
![image](function-nonvoid.png)
    
- Check out the example below to see the general layout of a function. In this example, we are **DEFINING** **a function** (“documenting the recipe”) called `makeSandwich`.
    - It does **return** a value here: one full sandwich.
    - *Why is this useful in real life? Why is this useful in code?*
    
![image](function-example.png)
      
{:.highlight}
For a more in-depth description of the **recipe analogy**, check out this blog post: [JavaScript Functions Explained by Making a Recipe](https://www.codeanalogies.com/javascript-functions-explained#javascript)
  
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


---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide), [The Modern JavaScript Tutorial](https://javascript.info/), and [CodeAnalogies Blog](https://www.codeanalogies.com/).
{: .fs-2 }
