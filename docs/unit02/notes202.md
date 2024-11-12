---
layout: notes
title: "📓2.2: Positioning" 
parent: "2️⃣ Advanced CSS"
nav_order: 2
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---

## CSS Positioning Modes

By now you have had quite a bit of practice moving elements around the screen using things like `margin`, `padding`, and `flex`box. These techniques have all relied on CSS's default **positioning-mode**: `static`. Static means the elements are placed one after the other, thus following "normal flow" of the HTML document.

![image]([https://static.techno-science.net/illustration/Libre/2024/09/30/rrpzIHZGQd6Y0KK64MEc0Q.jpg](https://media.istockphoto.com/id/1700005801/vector/cute-female-scientist-cartoon-character-conducting-static-electricity-experiment.jpg?s=612x612&w=0&k=20&c=0hlDFxaX-PhVgKgKZiDvbYon_6wkyDcRIR6Qmp63PyE=))

This default positioning-mode is intuitive, and you'll continue using it for almost all of your layout needs. However, there are other methods at your disposal that can be very useful in some situations.

#### Lesson overview
{:.no_toc}

This section contains a general overview of topics that you will learn in this lesson.

- You'll learn how to use `relative` positioning.
- You'll learn how to use `absolute` positioning.
- You'll learn how to use `fixed` positioning.
- You'll know the difference between each property and how to combine them.

![image](figures/positioned-elements-terminology.png)

### Relative Positioning

The default positioning mode that you've gotten used to is **static**. The difference between static and relative is fairly simple:
* `position: static` is the default position of every element, and unless this `position` property is changed from `static`, the properties `top`, `right`, `bottom`, and `left` do not affect the position of the element. 
* `position: relative` on the other hand is pretty much the same as static, but properties `top`, `right...(etc.)` **displace** the element _relative to its normal position_ in the flow of the document.

![image](figures/css-relative-positioning.png)

![image](figures/relative-positioning-offsets.png)

### Absolute Positioning

<div class="imp" markdown="block">
  
`position: absolute` allows you to **position something at an exact point** on the screen without disturbing the other elements around it. Using an absolute positioning scheme enables specifying the location anywhere on the screen with the  `top`, `right`, `bottom`, and `left` properties: 

```css
.absolute {
  position: absolute;
  top: 100px; /* 100px AWAY from TOP edge of page */
  left: 50%; /* 50% AWAY from LEFT edge of page */
}
```

</div>

> More specifically, using absolute positioning on an element will **remove that element** from the **normal document flow** while being positioned _relative to an ancestor element_. To put it in other words: elements that are removed from the normal flow of the document _do not affect other elements_ and are also not affected by other elements.

![image](figures/css-absolute-positioning.png)

This property is really useful when you want to position something at an **exact point** on the screen, without disturbing any of the other elements on the page. 

{:.highlight}
A couple of good use cases for **absolute positioning** are:
- Modals (pop up windows)
- Image with a caption on it
- Icons on top of other elements
- 🎨 If you're making CSS art (_our next project!_)

In the following example, we are using absolute positioning to display text _over_ an image.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="css,result" data-slug-hash="poWyWeJ" data-editable="true" data-user="TheOdinProjectExamples" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">

<span>See the Pen <a href="https://codepen.io/TheOdinProjectExamples/pen/poWyWeJ">
Absolute Position | CSS Positioning</a> by TheOdinProject (<a href="https://codepen.io/TheOdinProjectExamples">@TheOdinProjectExamples</a>)
on <a href="https://codepen.io">CodePen</a>.</span>

</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

{:.warning}
**Disclaimer:** Absolute positioning has very specific use cases and if possible, using `flex` or `grid` layout schemes should be prioritized. Absolute positioning should NOT be used to do entire page layouts.

#### "Relatively-Absolute" Positioning

![image](figures/css-relatively-absolute-positioning.png)

### Fixed Positioning

Fixed elements are also removed from the normal flow of the document and are positioned relative to the `viewport`. You basically use `top`, `right`, `bottom`, and `left` properties to position it, and it will _stay there as the user scrolls_. 

{:.highlight}
Fixed positioning is especially useful for things like **navigation bars** and **floating chat buttons** that you ALWAYS want displayed, regardless of where the user is on your page. 

![image](figures/css-fixed-positioning.png)

#### Sticky Positioning

Sticky elements will act like normal **static** elements until you _scroll past them_, then they start behaving like **fixed** elements. They are also _not taken out of the normal flow_ of the document. It might sound confusing, so check out this [sticky positioning example](https://codepen.io/theanam/pen/MPLBYy) that might clear things up for you. 

{:.highlight}
Sticky positioning is useful for things like **section-headings**. Remember being able to still see what category you're looking at while scrolling through a shop? This is how it's done!

---

#### Knowledge check
{: .no_toc }

<div class="task" markdown="1">

💬 **DISCUSS:** The following questions are an opportunity to reflect on key topics in this lesson. _If you can't answer a question, click on it to review the material._

- [What is the difference between static and relative positioning?](#static-and-relative-positioning)
- [What is absolute positioning useful for?](#absolute-positioning)
- [What is the difference between fixed and sticky positioning?](https://www.kevinpowell.co/article/positition-fixed-vs-sticky/)

</div>

#### Additional resources
{: .no_toc }

- Web Dev Simplified's [Learn CSS Position](https://www.youtube.com/watch?v=jx5jmI0UlXU) video is fast-paced but provides a good visual representation of different positioning behaviors. Go ahead and watch it.
- [MDN's docs on `position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position) covers all of the conceptual details about positioning.
- CSS trick's page [Absolute, Relative, Fixed Positioning](https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/) should give you a different insight on the topic. You should read it as well.
- Finally, Kevin Powell's article discusses the [difference between fixed and sticky positioning](https://www.kevinpowell.co/article/positition-fixed-vs-sticky/). It’s a great read to understand the difference better.
- [Understand the CSS Position Property With Practical Examples](https://www.makeuseof.com/css-position-property-practical-examples/) provides some different CSS methods for positioning elements.
- You can check out this helpful video resource on [CSS positioning from Slaying the Dragon](https://www.youtube.com/watch?v=MxEtxo_AaZ4&t=2s) for clear explanations and practical examples.

---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [The Odin Project](https://www.theodinproject.com/) and most images are from [Interneting is Hard](https://internetingishard.netlify.app/).

{: .fs-2 }

