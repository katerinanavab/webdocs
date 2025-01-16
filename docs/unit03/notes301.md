---
layout: notes
title: "📓3.1: Using the Bootstrap Framework" 
parent: "3️⃣ Bootstrap"
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
3. Specify the **repository name**: `CS1-Unit-3-Notes`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Take notes in this Codespace during class, coding along with the instructor.

</div>

---

## Developing Responsive Websites with Bootstrap

🥾 Bootstrap is a popular _front-end framework_ for developing **responsive** and **mobile-first** websites. 

![image](responsive_design.png)

<dl>
  <dt>Responsive</dt>
  <dd>Websites that <strong>automatically scale</strong> between devices — whether the device is a mobile phone, tablet, laptop, desktop computer, screen reader, etc.</dd>
</dl>

<dl>
  <dt>Mobile-First</dt>
  <dd>Websites that are primarily designed for mobile devices, then scales up from there (as opposed to being designed first for desktop, then trying to scale it down to mobile devices)</dd>
</dl>

### What is Bootstrap?
{:.no_toc} 

Bootstrap provides a collection of CSS and JavaScript-based design templates for **layout**, **typography**, **forms**, **buttons**, **navigation**, and other reusable **components**. You are free to use whichever Bootstrap components you choose, while adding your own on top. There are thousands of websites out there that are built on Bootstrap, but with their own design.

Bootstrap can be used to build websites of any scale, from small blogs to large corporate websites. Organizations that use Bootstrap include [NASA](https://www.nasa.gov/), [FIFA](https://www.fifa.com/en), [Newsweek](https://www.newsweek.com/), [VOGUE](https://www.vogue.com/) and many more.

#### Why Use Bootstrap?
* **Ease of Use:** Prebuilt styles and components.
* **Responsiveness:** Automatic adjustment to different screen sizes.
* **Consistency:** Uniform design across devices and browsers.
* **Customizability:** Override or extend styles as needed.
* **Fast Development:** Reusable components save time.

### Installing Bootstrap 5 via CDN

The simplest way to use Bootstrap is by including its **CDN** (Content Delivery Network) link in your HTML file.

1. Include the CDN link to Bootstrap's CSS code in the `<head>` section:
```html
<!-- Bootstrap CSS -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
```
1. To use interactive elements like **carousels** (slideshows) and **modals** (pop-up windows), include the CDN link to Bootstrap's JavaScript code at the _END_ of your `<body>` section:
```html
<!-- Bootstrap JS (optional) -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
```

---

## Bootstrap Tutorial


---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [Bootstrap 5 Tutorial - Quackit](https://www.quackit.com/bootstrap/bootstrap_5/tutorial/) and the [Bootstrap Documentation](https://getbootstrap.com/).
{: .fs-2 }
