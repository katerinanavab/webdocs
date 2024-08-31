---
layout: notes
title: "📓 Topic 1.2: HTML Foundations" 
parent: "1️⃣ Web Dev Foundations"
nav_order: 2
---

## Introduction to HTML

### Lesson overview

This section contains a general overview of topics that you will learn in this lesson.

- Get a basic overview of HTML, CSS and how they work together.

### HTML and CSS

HTML and CSS are two languages that work together to create everything that you see when you look at something on the internet. HTML is the raw data that a webpage is built out of. All the text, links, cards, lists, and buttons are created in HTML. CSS is what adds *style* to those plain elements. HTML puts information on a webpage, and CSS positions that information, gives it color, changes the font, and makes it look great!

Many great resources out there keep referring to HTML and CSS as *programming languages*, but if you want to get technical, labeling them as such is not quite accurate, because they are only concerned with presenting information. They are not used to program any logic. JavaScript, which you will be learning in the next section, is a programming language because it's used to make webpages do things. Yet, there is quite a lot you can do with just HTML and CSS, and you will definitely need them both. The following lessons focus on giving you the tools you need to be successful once you get to the JavaScript content as you continue through our curriculum!

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Read [HTML vs CSS vs JavaScript](https://brytdesigns.com/html-css-javascript-whats-the-difference/). It's a quick overview of the relationship between HTML, CSS, and JavaScript.

</div>

### Knowledge check

The following questions are an opportunity to reflect on key topics in this lesson. If you can't answer a question, click on it to review the material, but keep in mind you are not expected to memorize or master this knowledge.

- [What do HTML and CSS stand for?](https://brytdesigns.com/html-css-javascript-whats-the-difference/#What_is_HTML)
- [Between HTML and CSS, which would you use for putting paragraphs of text on a webpage?](#html-and-css)
- [Between HTML and CSS, which would you use for changing the font and background color of a button?](#html-and-css)
- [What is the difference between HTML, CSS and JavaScript?](https://brytdesigns.com/html-css-javascript-whats-the-difference/)

### Additional resources

This section contains helpful links to related content. It isn't required, so consider it supplemental.

- [FreeCodeCamp article](https://www.freecodecamp.org/news/html-css-and-javascript-explained-for-beginners/) goes into a little more depth than the assigned one. It covers things we'll be teaching explicitly in later lessons though, so don't worry about memorizing any of the details.

- Save [DevDocs.io](https://devdocs.io) as a bookmark for future reference. It's a massive API documentation collection maintained by [FreeCodeCamp](https://freecodecamp.org). Read the 'Welcome' message for more information.

---
## Elements and Tags

HTML (HyperText Markup Language) defines the structure and content of webpages. We use HTML elements to create all of the paragraphs, headings, lists, images, and links that make up a typical webpage. In this lesson, we will explore how HTML elements work.

### Lesson overview

This section contains a general overview of topics that you will learn in this lesson.

- Explain what HTML tags are.
- Explain what HTML elements are.

### Elements and tags

Almost all elements on an HTML page are just pieces of content wrapped in opening and closing HTML tags.

Opening tags tell the browser that this is the start of an HTML element. They are comprised of a keyword enclosed in angle brackets `<>`. For example, an opening paragraph tag looks like this: `<p>`.

Closing tags tell the browser where an element ends. They are almost the same as opening tags; the only difference is that they have a forward slash before the keyword. For example, a closing paragraph tag looks like this: `</p>`.

A full paragraph element looks like this:

```html
<p>some text content</p>
```

Let's break this down:

- `<p>` is the opening tag.
- `some text content` represents content wrapped within the opening and closing tags.
- `</p>` is the closing tag.

You can think of elements as containers for content. The opening and closing tags tell the browser what content the element contains. The browser can then use that information to determine how it should interpret and format the content.

HTML has a [vast list of predefined tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) that you can use to create all kinds of different elements. It is important to use the correct tags for content. Using the correct tags can have a big impact on two aspects of your sites: how they are ranked in search engines; and how accessible they are to users who rely on assistive technologies, like screen readers, to use the internet.

Using the correct elements for content is called semantic HTML. We will explore this in much more depth later on in the curriculum.

### Void Elements

Some HTML elements do not have a closing tag. These elements just have a single tag, like: `<br>` or `<img>`. They are known as void elements because they are void of any content, there is nothing inside of them. No closing tag means they can't wrap content like other tags do.

You might also see these referred to as self-closing tags. But those are just void elements with a forward slash(/) at the end like: `<br />` or `<img />`. You're likely to see self-closing tags used often for historical reasons. Browsers will be able to render them just fine, but the latest version of the HTML specification discourages their use and considers them invalid.

### Assignment

<div class="lesson-content__panel" markdown="1">

1. Watch Kevin Powell's [Introduction to HTML Video](https://www.youtube.com/watch?v=LGQuIIv2RVA).

</div>

### Knowledge check

The following questions are an opportunity to reflect on key topics in this lesson. If you can't answer a question, click on it to review the material, but keep in mind you are not expected to memorize or master this knowledge.

- [What is an HTML tag?](#elements-and-tags)
- [What are the three parts of an HTML element?](#elements-and-tags)

### Additional resources

This section contains helpful links to related content. It isn't required, so consider it supplemental.

- [Don't Fear the Internet's video about HTML](https://player.vimeo.com/video/24549728)

#### Acknowledgement

Content on this page is adapted from [The Odin Project](www.theodinproject.com).
{: .fs-2 }
