---
layout: notes
title: "📓NOTES 4.3: Conditionals & Loops" 
parent: "4️⃣ JavaScript"
nav_order: 3
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---

## Program Control Flow

![image-small](river-flow.webp)

**Control flow** or flow of control is a fundamental concept that simply shows the _order_ in which your program’s code is being _executed_. 
> 📣 It's basically you dictating or telling your program’s code “Hey this is how I want you to run under various scenarios or conditions until a particular condition is being met”.
 
<html>
 <dl>
  <dt>Control Statements</dt>
  <dd>Structures of code that lets your code execute an action depending on the context of the scenario or condition.</dd>
 </dl>
</html>

![image](flow-control.png)

{:.highlight}
**Flow control statements** affect the _execution order_ of **statements** or instructions in a program. They are often used to make _decisions_, _repeat_ blocks of code, and _jump_ to specific sections of code.

---

## Selection (Conditionals)

Sometimes, we need to _perform different actions_ based on different **conditions**. 

<div class="imp" markdown="block">
 
❓ A **CONDITION** in code is like a _question_...
❕ Where **BOOLEAN** values are the possible _answers_:
- `true` - means "yes", "correct" or "the truth".
- `false` - means "no", "wrong" or "not the truth".

</div>

### Comparison Operators

We know many comparison operators from math, which can be used in code to build **conditional expressions**. 

- **Greater/Less than:** <code>a &gt; b</code>, <code>a &lt; b</code>
- **Greater/Less than or Equal to:** <code>a &gt;= b</code>, <code>a &lt;= b</code>
- **Equal:** `a == b`
  > ⚠️ The double equality sign `==` means the _equality test_, while a single one `a = b` means a variable _assignment_!
- **NOT Equal:** `a != b`
  > In math, the notation is <code>&ne;</code>

All expressions that include **comparison operators** get _evaluated_ and return a **boolean** value: either `true` or `false`.

For example:

```js 
console.log( 2 > 1 ); 
console.log( 2 == 1 );
console.log( 2 != 1 ); 
```

A comparison **result** can be _assigned_ to a variable, just like any value:

```js
let result = 5 > 4; // assign the result of the comparison
console.log( result ); 
```

#### String comparison
{:.no_toc}

To see whether a **string** is greater than another, JavaScript uses the so-called "dictionary" or "lexicographical" order. In other words, strings are compared letter-by-letter.

For example:

```js 
console.log( 'Z' > 'A' ); 
console.log( 'Glow' > 'Glee' ); 
console.log( 'Bee' > 'Be' ); 
```

### `if` Statements

The `if(...)` statement _evaluates_ a **condition** in parentheses and, if the result is `true`, _executes_ a block of code. It is considered good practice to wrap the code block inside curly braces:

```js
if (age == 16) {
  console.log( "Sweet sixteen! 🥳" );
}
```
> In the example above, the condition is a simple _equality check_ ("is the **value** of the `age` **variable** equal to 18?"), but it can be much more complex.


#### Boolean conversion
{:.no_toc}

The `if (…)` statement _evaluates_ the expression in its parentheses and _converts_ the result to a **boolean**.

<div class="imp" markdown="block">

**What is "_Truthiness_"?**
- The number `0` or `0.0`, an empty string `""`, `null`, `undefined`, and `NaN` all get converted to `false`. Because of that they are called "_falsy_" values.
- Other values become `true`, so they are called "_truthy_".

</div>

So, the code under this condition would never execute:

```js
if (0) { // 0 is falsy
  ...
}
```

...and inside this condition -- it always will:

```js
if (1) { // 1 is truthy
  ...
}
```

<!--

### "Truthiness"

When we use `if()` statements, we are not always going to be able to plug in a variable that already holds the **value** of `true` or `false`. Many times, we must plug in a **statement** that will be _evaluated_ by JavaScript as `true` or `false`.

For example, do you know if the value `0` is `true` or `false`?

This is not a philosophy question – JavaScript has an answer. This happens because JavaScript is a _weakly typed_ language. This means that in the context of an `if()` statement, it will convert other variable values to `true` or `false` in order to run the code. This is known as determining the “truthiness” of a value.

> This is similar to the legal system! Although it is POSSIBLE that there will be one piece of evidence that makes the “guilty” or “not guilty” sentence obvious, it is also likely that a judge or jury will need to _evaluate_ the evidence and make a decision.

For this analogy, let's assume a `true` statement is one that will lead to the conviction of the accused car theft, while a `false` statement will let him/her walk free. 

```js
let evidence = "Fingerprints";
 
if (evidence) {
  convict();
}
 
else {
  release();
}
```
> `convict()` and `release()` are made-up functions. In this case, since `evidence` has a non-zero/non-empty value, the `if()` statement _evaluates_ to `true`, so the judge would convict the car thief. 

Here’s an interactive diagram of this scenario:

<iframe src="https://blog.codeanalogies.com/wp-admin/admin-ajax.php?action=h5p_embed&id=19" width="680" height="322" frameborder="0" allowfullscreen="allowfullscreen" title="True Value in If Statement"></iframe><script src="https://blog.codeanalogies.com/wp-content/plugins/h5p/h5p-php-library/js/h5p-resizer.js" charset="UTF-8"></script>

-->


#### The `else` clause
{:.no_toc}

The `if` statement may contain an optional `else` block. It executes when the condition is falsy.

```js 
if (age == 16) {
  console.log( "Sweet sixteen! 🥳" );
}
else {
  console.log( "You can't have a sweet sixteen party..." ); // any value except 16
}

```

#### Several conditions: `else if`
{:.no_toc}

Sometimes, we'd like to test _several variants_ of a condition. The `else if` clause lets us do that.

```js 
if (age < 18) {
  console.log( "Too young to vote..." );
}
else if (age > 18) {
  console.log( "Old enough to vote!" );
}
else {
  console.log( "It's the first year you can vote!" );
}
```
> In the code above, JavaScript first checks `year < 2015`. If that is falsy, it goes to the next condition `year > 2015`. If that is also falsy, it shows the last `alert`.

{:.highlight}
After any `if` block, there can be as many `else if` blocks as needed! The final `else` is optional, which can be considered the "_otherwise_..." situation. 

<div class="task" markdown="block">

Complete **steps 7-14** in the following _interactive tutorial_: 
[🏗️ JS Construction Site](https://www.codeanalogies.com/jsconstruction/)

</div>

---

## Iteration (Looping)

We often need to **repeat** actions. For example, outputting goods from a list of goods, one after another. *Loops* are a way to repeat the same code multiple times.


### `while` Loops 

The `while` loop has the following syntax:

```js
while (condition) {
  // code
  // so-called "loop body"
}
```

While the `condition` is truthy, the `code` from the loop body is executed.

For instance, the loop below outputs `i` while `i < 3`:

```js 
let i = 0;
while (i < 3) { // shows 0, then 1, then 2
  alert( i );
  i++;
}
```

A single execution of the loop body is called *an iteration*. The loop in the example above makes three iterations.

If `i++` was missing from the example above, the loop would repeat (in theory) forever. In practice, the browser provides ways to stop such loops, and in server-side JavaScript, we can kill the process.

Any expression or variable can be a loop condition, not just comparisons: the condition is evaluated and converted to a boolean by `while`.

For instance, a shorter way to write `while (i != 0)` is `while (i)`:

```js 
let i = 3;
while (i) { // when i becomes 0, the condition becomes falsy, and the loop stops
  alert( i );
  i--;
}
```


### `for` Loops

The `for` loop is more complex, but it's also the most commonly used loop.

It looks like this:

```js
for (begin; condition; step) {
  // ... loop body ...
}
```

Let's learn the meaning of these parts by example. The loop below runs `alert(i)` for `i` from `0` up to (but not including) `3`:

```js
for (let i = 0; i < 3; i++) { // shows 0, then 1, then 2
  alert(i);
}
```

Let's examine the `for` statement part-by-part:

| part  |          |                                                                            |
|-------|----------|----------------------------------------------------------------------------|
| begin | `let i = 0`    | Executes once upon entering the loop.                                      |
| condition | `i < 3`| Checked before every loop iteration. If false, the loop stops.              |
| body | `alert(i)`| Runs again and again while the condition is truthy.                         |
| step| `i++`      | Executes after the body on each iteration. |

The general loop algorithm works like this:

```
Run begin
→ (if condition → run body and run step)
→ (if condition → run body and run step)
→ (if condition → run body and run step)
→ ...
```

That is, `begin` executes once, and then it iterates: after each `condition` test, `body` and `step` are executed.

If you are new to loops, it could help to go back to the example and reproduce how it runs step-by-step on a piece of paper.

Here's exactly what happens in our case:

```js
// for (let i = 0; i < 3; i++) alert(i)

// run begin
let i = 0
// if condition → run body and run step
if (i < 3) { alert(i); i++ }
// if condition → run body and run step
if (i < 3) { alert(i); i++ }
// if condition → run body and run step
if (i < 3) { alert(i); i++ }
// ...finish, because now i == 3
```

#### Inline Variable Declaration
{:.no_toc}

Here, the "counter" variable `i` is declared right in the loop. This is called an "inline" variable declaration. Such variables are visible only inside the loop.

```js 
for (let i = 0; i < 3; i++) {
  alert(i); // 0, 1, 2
}
alert(i); // error, no such variable
```

Instead of defining a variable, we could use an existing one:

```js 
let i = 0;

for (i = 0; i < 3; i++) { // use an existing variable
  alert(i); // 0, 1, 2
}

alert(i); // 3, visible, because declared outside of the loop
```

#### Breaking the loop
{:.no_toc}

Normally, a loop exits when its condition becomes falsy.

But we can force the exit at any time using the special `break` directive.

For example, the loop below asks the user for a series of numbers, "breaking" when no number is entered:

```js 
let sum = 0;

while (true) {

  let value = +prompt("Enter a number", '');

  if (!value) break;

  sum += value;

}
alert( 'Sum: ' + sum );
```

The `break` directive is activated at the line `(*)` if the user enters an empty line or cancels the input. It stops the loop immediately, passing control to the first line after the loop. Namely, `alert`.

The combination "infinite loop + `break` as needed" is great for situations when a loop's condition must be checked not in the beginning or end of the loop, but in the middle or even in several places of its body.

#### Continue to the next iteration 
{:.no_toc}

The `continue` directive is a "lighter version" of `break`. It doesn't stop the whole loop. Instead, it stops the current iteration and forces the loop to start a new one (if the condition allows).

We can use it if we're done with the current iteration and would like to move on to the next one.

The loop below uses `continue` to output only odd values:

```js 
for (let i = 0; i < 10; i++) {

  // if true, skip the remaining part of the body
  if (i % 2 == 0) continue;

  alert(i); // 1, then 3, 5, 7, 9
}
```

For even values of `i`, the `continue` directive stops executing the body and passes control to the next iteration of `for` (with the next number). So the `alert` is only called for odd values.

#### Summary
{:.no_toc}

- `while ( )` - condition is checked before each iteration.
- `for ( ; ; )` - condition is checked before each iteration, additional settings available.
- To make an "infinite" loop, usually the `while(true)` construct is used. Such a loop, just like any other, can be stopped with the `break` directive.
- If we don't want to do anything in the current iteration and would like to forward to the next one, we can use the `continue` directive.


---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from the [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide), [The Modern JavaScript Tutorial](https://javascript.info/), and [CodeAnalogies Blog](https://www.codeanalogies.com/).
{: .fs-2 }
