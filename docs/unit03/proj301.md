---
layout: project
title: "💻PROJECT #3.1"
projectname: "Responsive Personal Website"
parent: "3️⃣ Bootstrap Framework"
nav_order: 5
---


### Overview & Setup

In this project, you will create a **responsive one-page personal website** that demonstrates your mastery of Bootstrap and the concepts covered in the tutorials. The project is open-ended to encourage creativity while giving you the opportunity to practice building a responsive and visually appealing website.

#### Project Goal
Design and develop a **one-page personal website** using Bootstrap classes and UI components. Your website should reflect your _personality_, _interests_, or _goals_ and include well-organized sections with responsive layouts.
> 💡 **INSPIRATION:** [Developer Portfolio Websites](https://github.com/emmabostian/developer-portfolios) → scroll down to links, open random pages, make notes of _design choices_ that resonate with you.

<div class="setup" markdown="block">

1. Go to the `CS1 Project 3.1` assignment on **Blackbaud** and follow the provided **GitHub Classroom** link.
  > 📁 Clicking the link generates a **private repository** for your project with the appropriate starter code. Note that **projects** are stored within the [BWL-CS Organization](https://github.com/BWL-CS), so you _cannot_ access it from the "Your Repositories" page!
2. Open the repository in a **Codespace** whenever you spend time working on the program, in class or at home. 
  > ⚠️ Always remember to `commit changes` after every coding session!
3. When your project is complete, **submit the link to your repository** in the `CS1 Project 3.1` assignment on Blackbaud.

</div>

--- 

### Instructions

#### Plan & Set Up Your Website

Decide on the _content_ and _structure_ of your website. At a minimum, your site should include the following sections:
- **Hero Section**: A welcoming section with your name, a title, and a short tagline.
- **About Me**: A section describing who you are, your interests, or your goals.
- **Portfolio/Showcase**: Highlight your work, hobbies, or achievements using cards, images, or a grid layout.

**Brainstorming Content Ideas**:
- **Hero Section**: Think about how you want to introduce yourself. Consider a tagline or quote that represents your values or aspirations.
- **About Me**: What makes you unique? Share your hobbies, favorite activities, or personal story. Include a profile picture.
- **Portfolio/Showcase**: If you have completed projects, hobbies, or any creative work, showcase them here. If not, create placeholders for future content.

Optional sections could include:
- **Skills**: Highlight your technical or personal skills.
- **Testimonials**: Add quotes or feedback from others.
- **Hobbies**: Showcase things you enjoy doing.
  
**Include Bootstrap**:
   - Add the Bootstrap CDN links to your `index.html` file, in the `<head>` section:
     ```html
     <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
     <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
     ```

#### Create Your Layout
2. **Hero Section**:
   - Use a full-width background image or gradient.
   - Add a large heading and a short tagline centered in the section.
3. **Grid-Based Layout**:
   - Use Bootstrap's grid system to create responsive layouts for your content.
   - Experiment with different column sizes for each section (e.g., `.col-6`, `.col-md-4`).
4. **Components**:
   - Use Bootstrap components like cards, buttons, badges, or alerts to make your site visually appealing.

#### Customize with CSS
1. Create a `custom.css` file in the `css/` folder to override Bootstrap styles and personalize your website.
2. _Example:_ Override the `.text-primary` class to change its color:
   ```css
   .text-primary {
       color: #ff5733 !important; 
   }
   ```
3. Apply your custom styles to make the website uniquely yours, such as changing font sizes, background colors, or adding padding.

#### Content and Images
1. Add meaningful content for each section.
2. Use images that reflect your personality, work, or interests.
3. Optimize images by resizing them to appropriate dimensions for the web.


--- 

### Minimum Requirement Checklist

Before submitting, ensure your website includes the following:

1. **Hero Section**:
   - [ ] Full-width background (color, image or gradient).
   - [ ] Large heading and a short tagline.

2. **About Me Section**:
   - [ ] Text content describing who you are, your interests, or your goals.
   - [ ] A profile image styled with Bootstrap classes (e.g., `rounded-circle`).

3. **Portfolio/Showcase Section**:
   - [ ] At least three items displayed.

4. **Responsive Design**:
   - [ ] Use Bootstrap's **grid system** to ensure your website adapts to different screen sizes.
   - [ ] Use Bootstrap **UI components** like cards or carousels.

5. **Custom CSS**:
   - [ ] Include a `style.css` file with at least one overridden Bootstrap class (e.g., `.text-primary`).

#### Bonus Challenges
- Add a **carousel** to showcase images or testimonials.
- Add a responsive **navigation bar** at the top of your website using Bootstrap's navbar component. Ensure links scroll to the corresponding sections of the page.
- Use Bootstrap's **scrollspy** to highlight the current section in the navbar as users scroll.
- Experiment with more Bootstrap components like alerts or badges.


{:.highlight}
**RESOURCES:** While working on this project or attempting the bonus features, you are encouraged to look up any Bootstrap `classes` or starter code! Refer to the [📖 Bootstrap Documentation](https://www.w3schools.com/css/), review our [📓 Unit 3 Notes](https://coderina.dev/webdocs/unit03). 

