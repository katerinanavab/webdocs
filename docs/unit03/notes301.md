---
layout: notes
title: "📓3.1: Using Bootstrap Classes" 
parent: "3️⃣ Bootstrap Framework"
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
3. Specify the **repository name**: `CS1-Unit-3-Notes` or `CS1-Bootstrap-Notes`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Take notes in this Codespace during class, coding along with the instructor.

</div>

---

## Developing Responsive Websites

🥾 Bootstrap is a popular _front-end framework_ for developing **responsive** and **mobile-first** websites. 

![image](responsive_design.png)

<html>
<dl>
  <dt>Responsive</dt>
  <dd>Websites that <strong>automatically scale</strong> between devices — whether the device is a mobile phone, tablet, laptop, desktop computer, screen reader, etc.</dd>
</dl>
</html>

<html>
<dl>
  <dt>Mobile-First</dt>
  <dd>Websites that are primarily designed for mobile devices, then scales up from there (as opposed to being designed first for desktop, then trying to scale it down to mobile devices)</dd>
</dl>
</html>

### What is Bootstrap?
{:.no_toc} 

Bootstrap provides a collection of `CSS` classes and JavaScript-based design templates for **layout**, **typography**, **forms**, **buttons**, **navigation**, and other reusable webpage **components**. You are free to use whichever Bootstrap components you choose, while adding your own on top! There are thousands of websites out there that are built on Bootstrap, but with their own customizations.

Bootstrap can be used to build websites of any scale, from small blogs to large corporate websites. Organizations that use Bootstrap include [NASA](https://www.nasa.gov/), [FIFA](https://www.fifa.com/en), [Newsweek](https://www.newsweek.com/), [VOGUE](https://www.vogue.com/) and many more.

#### Why Use Bootstrap?
{:.no_toc} 
* **Ease of Use:** Prebuilt CSS styles and components.
* **Responsiveness:** Automatic adjustment to different screen sizes.
* **Consistency:** Uniform design across devices and browsers.
* **Customizability:** Override or extend styles as needed.
* **Fast Development:** Reusable components save time.

### Installing Bootstrap 5 via CDN Link

The simplest way to load/use Bootstrap is by including its **CDN link** in your HTML file. 

📥 A **CDN** (**C**ontent **D**elivery **N**etwork) is a distributed network of servers strategically located in different parts of the world to deliver content, such as files, images, and scripts, to users faster and more reliably.

1. Include the CDN link to Bootstrap's CSS code in the `<head>` section:
    ```html
    {% raw %}
        <!-- Bootstrap CSS -->
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    {% endraw %} 
    ```
1. To use interactive elements like **carousels** (slideshows) and **modals** (pop-up windows), include the CDN link to Bootstrap's JavaScript code too:
    ```html
    {% raw %}
        <!-- Bootstrap JS (optional) -->
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
    {% endraw %} 
    ```

---

## Bootstrap Tutorial

### 📦 Containers

Containers are a fundamental building block of Bootstrap that **contain**, **pad**, and **align** your content within a given device or viewport. Bootstrap requires a *containing element* to wrap elements and contain its <a href='#grid'>Grid System</a> (more on this later on in the tutorial). Bootstrap's container **classes** were created specifically for this purpose.

Bootstrap 5 includes three different container types:
* Fixed (`class="container"`)
* Fluid (`class="container-fluid"`)
* Responsive (see [Bootstrap Documentation](https://getbootstrap.com/docs/5.3/layout/containers/))

#### Fixed Containers
{:.no_toc}
A fixed container is a (responsive) **fixed width** container. As you resize your browser, its width remains intact, until it passes a certain screen size _breakpoint_, at which time it will resize to the new width for that break point.

```html
<div class="container"></div>
```

#### Fluid Containers
{:.no_toc}

A fluid container spans the **full width of the viewport**. It will expand and contract fluidly as you _resize_ the browser. This is in contrast to the fixed width container which will appear to "jump" to the new size as you pass a given break point.

```html
<div class="container-fluid"></div>
```

### 🖼️ Responsive Images

Bootstrap provides classes that can be used when working with the `<img>` element. Most of these are utility classes that can be applied to any element (not just images). However, there is a class specifically for responsive images.

Bootstrap provides the `.img-fluid` class to make an image **scale** appropriately across devices. Behind the scenes, this class applies the `max-width: 100%` and `height: auto` **CSS properties** to the image. This ensures that the image scales to the parent element.

To see an image scale, insert an image element of your choice into a container, then try resizing your browser window:
```html
<img src="" class="img-fluid">
```

#### Image Borders

You can use Bootstrap to render images with rounded corners or as a circle. This is acheived with the `.rounded-*` utility classes.

You can also use the `.img-thumbnail` class to give it a rounded 1 pixel border.

```html
<img src="" class="rounded">
<img src="" class="rounded-circle">
<img src="" class="rounded-pill">
<img src="" class="img-thumbnail">
```

{:.highlight}
The **border radius** utility classes like `.rounded` and `.rounded-circle` can be applied to _any element_ (not just images)!

#### Centering Images

You can include Bootstrap's `.text-center` class on the image's **parent** element to center an image.
```html
<div class="container text-center">
    <img src="" class="">
</div>
```

Alternatively, you can force the image to "behave" like a block with Bootstrap's class `.d-block` class, which applies the CSS rule `display: block;`. Then, add Bootstrap's `.mx-auto` to center the block image, which sets `margin: auto;`.

```html
<img src="" class="mx-auto d-block">
```

### 🎨 Style Utilities

#### Typography

#### Colors 

#### Borders

### 🔲 Grid System Layouts
<span id='grid'></span>

Grid systems enable you to create advanced layouts using **rows** and **columns**. The Bootstrap grid system can have up to **12 columns**, and you can specify how these columns scale for different viewport sizes.


---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [Bootstrap 5 Tutorial - Quackit](https://www.quackit.com/bootstrap/bootstrap_5/tutorial/) and the [Bootstrap Documentation](https://getbootstrap.com/).
{: .fs-2 }
