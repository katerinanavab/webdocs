---
layout: notes
title: "📓1.1: Web Development" 
parent: "1️⃣ Web Dev Foundations"
nav_order: 1
---

## Table of Contents
{: .no_toc .text-delta }

{: .fs-2 }
- TOC
{:toc}

---
## Introduction to Web Development
What do web developers do? In short, they **build and maintain websites**.

Web developers often work for clients who are trying to get their product or service onto the web. The work is typically project-focused and involves collaborating with a team to coordinate the client’s needs into the end product. The client could be a tech company, an organization, or a government. The work could involve `front-end`, `back-end`, or `full-stack` web development.

Web development could be a good profession for you if you like **solving logical problems**, **building useful things**, and **experimenting with new technologies**. Web developers are in high demand, generally have a good work-life balance, and command comfortable salaries. Google your specific location to get a better sense of your local web development job opportunities.

### Types of Web Developers
Earlier, we mentioned that web development work could be in the front end, the back end, or the full stack. What exactly do these terms mean?

![image](https://www.toptal.com/custom-software-development/wp-content/uploads/2016/08/front-end-vs-back-end-750x375.jpg)

* The `front end` is the stuff you see on the website in your browser, including the presentation of content and user interface elements like the navigation bar. Front-end developers use HTML, CSS, JavaScript, and their relevant frameworks to ensure that content is presented effectively and that users have an excellent experience.

* The `back end` refers to the guts of the application, which live on the server. The back end stores and serves program data to ensure that the front end has what it needs. This process can become very complicated when a website has millions of users. Back-end developers use programming languages like Java, Python, Ruby, and JavaScript to work with data.

* `Full-stack developers` are comfortable working with both the front and back ends.

### X-Ray Goggles Activity

🥽 [X-Ray Goggles](https://x-ray-goggles.mouse.org/) is a free tool from Mozilla that lets you remix any page that you find on the Internet. (_Note: it doesn’t change the way others see the page, it only changes the way that you see it._) 

To use X-ray Goggles you need to install it in your Chrome bookmarks bar. Then you can launch it on any webpage. When you launch X-ray Goggles you will be able to **select images and text** on a page and see the **code** behind your selection. X-ray Goggles will let you then **alter the code** to display new things on that page!

{:.highlight}
🌐 Use **GOOGLE CHROME** as your web browser!!! You may have to use a _personal_ Chrome profile rather than your BWL account for this particular activity. 

#### PART A: Introduce Developer Tools 
{:.no_toc}

Open any website, **right click** (or hold `⌃ CONTROL` + **click** on Mac) anywhere on the page, then select `View Page Source` to show the code behind a website. Another thing you can do is select `Inspect` to open up **Chrome's Developer Tools**, which includes the code behind the website PLUS some extra features that web developers may use to test/investigate code.

> Feel free to check these out, but don’t worry – all the code behind websites is written in **three different new languages** so it may look pretty overwhelming at first.
> 
> We’ll learn how to play around with `Inspect` and more Dev Tools later on in the course, but for now, we'll use something more user friendly to explore the code behind websites.

#### PART B: Install X-Ray Goggles
{:.no_toc}

<div class="task" markdown="block">

1. Follow instructions on the <a href="https://x-ray-goggles.mouse.org/"><button type="button" name="button" class="btn">X-Ray Goggles</button></a> page to install the X-Ray Goggles Extension in your **Bookmarks Toolbar**.

2. Staying on the X-Ray Goggles website, click the **Bookmark** you just installed to activate it.

3. Use X-Ray Goggles to change 🔤**TEXT**🔤 on the page.
  > 💡 **HINT:** Text is usually contained in HTML elements like `p`, `h1`, `h2`, `h3`, etc

4. Use X-Ray Goggles to change 🖼️**IMAGES**🖼️ on the page:   
   a. Go to [Google Image Search](https://images.google.com/) and find an image you would like to use, `⌃ CONTROL` + **click** on the image and select `Copy Image Address`. This gives you the **URL** (_Uniform Resource Locator - basically an address/location on the web_) of the image.

   b. Activate X-Ray Goggles, then click on the image on the page that you would like to change.
     > **NOTE:** Some pictures might actually be a contained in a different kind of HTML element like a link, iframe, etc. so make sure you pick something that is contained in an `<img>` tag specifically!

   c. Look for the `src=" ` then delete everything until the next quotation mark (_the old image's URL/address_).

   d. Paste the copied image address (_the new image's **source**_) between the quotations that follow the `src=`

   e. Then click `Update` and your image should change on the website!

</div>


#### PART C: Hack the News
{:.no_toc}

First, discuss the definition of "hacking": [What is Hacking?](https://wiki.mozilla.org/Webmaker/Teach/Terminology#Hack)

<div class="task" markdown="block">

1. Navigate to one of the following **news websites**: [BBC](https://www.bbc.com/), [Gothamist](https://gothamist.com/), [Vogue](https://www.vogue.com/fashion), [Bleacher Report](https://bleacherreport.com/).
  > You can try another news site if you prefer, but I've confirmed that these options work well with X-Ray Goggles.
  > 
  > Don’t worry — you’re not actually hacking the site for others — just yourself. You’re changing a _local version_ of the site that only you can see.
  > 
  > 🚨 **Be careful not to reload the page** or you will lose your changes!

2. Decide on one of these fun remix themes (or one of your own)
  > **The year 2525:** What’s on the front page of the paper in the year 2525? Are humans living on the moon yet? Have robots taken over? You decide!
  > 
  > **Your Birthday:** Write the headlines for the day were born. Do some research to find out what happened that day. What was the weather was like? What song was most popular?
  > 
  > **Zombie Apocalypse:** It’s the day after the zombies have risen from the dead – what is on the cover of the newspaper? Interviews with zombies? Survival tips? Ideas about what caused the spread of Zombie-ism?

3. **Activate the Goggles** by clicking on your Bookmark. Now when you mouse over elements of the news page, you’ll see the code underneath.

4. Change all of the **text** and swap in new **images**.
  > Try changing the headlines and rewriting some of the stories. The more content you change, the more believable your remix will be. 

5. 📸 Take a **screenshot** (Mac shortcut: `⌘ COMMAND` + `⇧ SHIFT` + `3`) and email it to me!

</div>

---

## Coding Motivation
Learning to code is incredibly rewarding but can also be difficult and frustrating. The strongest assets you can have as a student are a desire to build, a problem-solving mind, and persistence in the face of setbacks.

The web development industry has a long history of successful developers with varying backgrounds, so people tend to care more about what you’ve actually **built** than how you got there.

<div class="task" markdown="1">

1. Read our course website's [Mindset & Motivation Tips](https://coderina.dev/webdocs/docs/ref/mindset.html) page and follow along with the activities in class.
1. Check out the post ["Why Learning to Code is **So Damn Hard**"](https://web.archive.org/web/20230630111131/https://www.thinkful.com/blog/why-learning-to-code-is-so-damn-hard/) so you have a good idea of what the journey ahead is like.
1. Read the [Wikipedia entry on web design](https://en.wikipedia.org/wiki/Web_design) that describes the breadth of the web development profession.
1. Read Udacity's blog post on [front-end, back-end and full stack developers.](https://www.udacity.com/blog/2020/12/front-end-vs-back-end-vs-full-stack-web-developers.html)

</div>

#### Additional Resources
{: .no_toc }

- [Quora: How can I Become a Really Good Web Developer?](http://www.quora.com/Computer-Programming/How-can-I-become-a-really-good-Web-Developer-starting-from-now-at-age-20-before-age-25)
- [Quora: What makes a great web developer?](http://www.quora.com/What-makes-a-great-web-developer)
- [Jared the Nerd: What makes a good Developer?](http://jaredthenerd.com/2013/05/What-Makes-A-Good-Developer/)
- [FreeCodeCamp: Things I Wish Someone Had Told Me When I Was Learning How To Code](https://www.freecodecamp.org/news/things-i-wish-someone-had-told-me-when-i-was-learning-how-to-code-565fc9dcb329/)
- [TechCrunch: Don't Believe Anyone who Tells you Learning to Code is Easy](http://techcrunch.com/2014/05/24/dont-believe-anyone-who-tells-you-learning-to-code-is-easy/)
- [Code Quizzes: Deliberate Programming Practice](https://codequizzes.wordpress.com/2013/04/28/deliberate-programming-practice/)

---

## GitHub Account Setup

<div class="task" markdown="block">

1. **Go to:** [GitHub Sign Up](https://github.com/signup)
2. Enter your `@gbwl.org` **school email**
3. Create a **password** that you'll remember 
4. Enter a **username** that follows this pattern: `FirstName` `LastInitial` `GradYear`
    > _For example:_ `KaterinaN2014`
    > 
    > DO NOT include your entire last name (_privacy reasons_)
5. After verifying your account, **let me know** so I can add you to the GitHub Classroom group!
   
</div>

#### Using a GitHub Template for class notes
{:.no_toc}

<div class="setup" markdown="block">

1. Go to the public template **repository** for our class: [BWL-CS HTML/CSS/JS Template](https://github.com/BWL-CS/html-css-js-template)
2. Click the <button type="button" name="button" class="btn btn-green">Use this template</button> button above the list of files then select `Create a new repository`
3. Specify the **repository name**: `CS1-Unit1-Notes`
4. Click <button type="button" name="button" class="btn btn-green">Create repository</button>
    > Now you have **your own personal copy** of this starter code that you can always access under the `Your repositories` section of GitHub! 
5. Now on your repository, click <button type="button" name="button" class="btn btn-green"> < > Code </button> and select the `Codespaces` tab
6. Click `Create Codespace on main` and wait for the environment to load, _then you're ready to code_!
7. 📝 Take notes in this Codespace during class, coding along with the instructor.

</div>

---

#### Acknowledgement
{: .no_toc }

Content on this page is adapted from [The Odin Project](https://www.theodinproject.com/).
{: .fs-2 }
