<!-- @format -->

PROJECT TODOS:

- Use AI
    - Review for accessibility, readability and maintainability
    - Adjust comments if needed
- Construct this README

- AI Prompt:

Review my HTML and SCSS files for accessibility, accountability, and maintainability.
Consider all files as an interconnected project before suggesting changes.

Files to review:
- index.html (main structure)
- ./assets/styles/scss/_settings.scss (styling)
- ./assets/styles/scss/_mixins.scss (styling)
- ./assets/styles/scss/main.scss (styling)

Please analyze the following aspects:

1. Accessibility:
   - ARIA labels and semantic HTML usage
   - Color contrast ratios
   - Keyboard navigation support
   - Alt text for images
   - Error handling

2. Accountability & Code Quality:
   - Unused CSS rules or variables
   - Magic numbers without explanation
   - Naming conventions consistency
   - Specificity issues in selectors

3. Maintainability:
   - CSS organization (variables, mixins, nesting depth)
   - Code duplication opportunities
   - Responsive design patterns

4. Documentation:
   - Suggest inline comments for complex logic
   - Document SCSS mixins and functions
   - Flag sections needing clarification

Please provide specific recommendations.

2nd prompt:

You are a frontend code reviewer focused on readability and maintainability. Review the following HTML and SCSS code with these principles in mind:

Class Naming Conventions:

- Class names must reflect purpose and functionality, not appearance (e.g., use .product-card instead of .blue-box, use .form-error-message instead of .red-text)
- Use semantic, descriptive names that clearly communicate what the element does
- Avoid abbreviations unless they're widely recognized in the domain
- Use kebab-case (lowercase with hyphens) for all class names
- Prefix utility or state classes with a consistent modifier (e.g., .is-active, .has-error, .is-disabled)

Structure & Organization:

- Group related styles logically by component or feature, not by property type
- Use comments to explain the "why" behind non-obvious styling decisions
- Maintain a clear separation between layout, component, and utility styles

HTML Readability:

- Keep indentation consistent and logical to reflect the DOM hierarchy
- Use data attributes for JavaScript hooks (e.g., data-js-toggle) separate from styling classes

SCSS Best Practices:

- Use variables for colors, spacing, typography, and breakpoints with descriptive names
- Keep mixins focused and reusable; document their parameters
- Avoid over-nesting; flatten selectors when they become too specific
- Use functions for calculations (e.g., spacing scales, color adjustments)

Overall Goals:

- Code should be understandable to another developer (or your future self) without extensive comments
- Changes to appearance should not require renaming classes
The codebase should scale without becoming unwieldy


# Frontend Mentor - Meet landing page solution

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
- [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
    - [AI Collaboration](#ai-collaboration)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it.

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```

```css
.proud-of-this-css {
	color: papayawhip;
}
```

```js
const proudOfThisFunc = () => {
	console.log("🎉");
};
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

### AI Collaboration

Describe how you used AI tools (if any) during this project. This helps demonstrate your ability to work effectively with AI assistants.

- What tools did you use (e.g., ChatGPT, Claude, GitHub Copilot)?
- How did you use them (e.g., debugging, generating boilerplate, brainstorming solutions)?
- What worked well? What didn't?

**Note: Delete this note and the content above if you didn't use AI, or replace with your own experience.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
