<!-- @format -->

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
    - [CSS](#what-i-learned--css)
    - [SASS](#what-i-learned--sass)
    - [CSS & SASS](#what-i-learned--css--sass)
    - [VSCode](#what-i-learned--vscode)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

This screenshot shows:

- `:focus-visible` state for `<button>What is it?</button>`
- `:hover` state for the third image `<img alt="man in video chat" />`

![screenshot](./screenshot.png)

### Links

- [Solution](https://github.com/ayx234/FM-Meet_Landing_Page)
- [Live site](https://ayx234.github.io/FM-Meet_Landing_Page)

## My process

### Built with

- Semantic HTML5 markup
- Fluid Responsive Design
  - Fluid Typography
  - Fluid Spacing
- Mobile-first workflow
- Flexbox
- CSS Grid
- [SASS](https://sass-lang.com/) - CSS Preprocessor
  - variables
  - Mixins

### What I learned

#### What-I-Learned--CSS

- Class names should describe purpose and functionality not appearance.
  - E.g. `.primary-color` not `.green` and `.price-card` not `.yellow-card`.
- Use variables for breakpoints.
  - Makes changing the breakpoint easier for multiple @media queries
- Use variables for your values of colors, spacing, fonts etc...
- If you use magic numbers, explain why in a comment (document why).

#### What-I-Learned--SASS

#### Importing Variables

After importing a file that has variables. We need a "namespace" to preceed the variables in order to use them. The default name space is the name of the file without the `_`.

\_variables.scss:

```CSS
$my-color: value;

```

main.scss:

```CSS
@use 'variables'

.body {
   color: variables.$my-color;
}
```

#### Use Mixins to Reduce Code Duplication

Mixins help apply the DRY principle (Dont' Repeat Yourself).

a group of properties that are used together more than once in the code can be turned into a mixin.

\_mixins.scss:

```CSS

// ----- Text

@mixin text-preset-1 {
  // Usage: Page headings (h1).
  font-size: variables.$my-value;
  line-height: 110%;
  letter-spacing: 0;
}

// ----- Button states
@mixin button-hover-color($bg-color, $outline-color) {
  background-color: $bg-color;
  outline: ##px outline-style-value $outline-color;
}

// ----- Drop shadows

@mixin shadow-text {
  text-shadow: #px #px #px colorValue;
}
```

main.scss:

```CSS
h1,
h2 {
  @include mixins.shadow-text;
}

h1 {
  @include mixins.text-preset-1;
}

.button:is(:hover, :focus-visible) {
  outline-offset: variables.$outline-offset;

  &[data-color="cyan"] {
    @include mixins.button-hover-color(
      variables.$cyan-300-hover,
      variables.$cyan-300-hover
    );
  }
}
```

#### What-I-Learned--CSS-&-SASS

- Using CSS variables is preferred to using SASS variables for:
  - Dynamic and Runtime Flexibility
    - CSS variables can be changed at runtime using JavaScript or by updating styles dynamically.
  - Cascade and Inheritance
    - With CSS variables, you can change values based on media queries directly in CSS without recompiling. Sass variables can't do this—they're baked into the compiled output.
  - Interoperability
    - CSS variables work seamlessly across different preprocessors and frameworks, whereas Sass variables are Sass-specific. If you ever need to mix technologies or migrate away from Sass, CSS variables provide better portability.
- Decide ahead if you want to work with CSS variables or SCSS variables. From experience in this project, changing variables after completing the site might require increased mental effort and is prone to bugs. In my case I used regex and vscode folder search and replace (workspace search & replace?) using ctrl + shift + h.

#### What-I-Learned--VSCODE

Search and replace can be activated across the working folder using `ctrl + shift + h.`

### Continued development

#### Continued-Development--HTML

- Accessibilty
- Semantic HTML

#### Continued-Development--CSS

- Layouts
- Designing
- Animations
- New features and properties

#### Continued-Development--SASS

- Folder structures
- Functions
- Mixins
- More Basics

### Useful resources

- Generation of `clamp()` values for fluid `font-size`s and spacing [Utopia.fyi](https://utopia.fyi/)

### AI Collaboration

I used VScode Copilot chat that used Calude 4.5 as a model.

This project comes with an AGENTS.md and a CLAUDE.md that instruct AI modules to give suggestions for where code is to be changed instead of making changes.

#### Prompts

I used two prompts as follows

#### Prompt 1

```
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
```

#### Prompt 2

```
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
```

## Author

- Github - [Ali Al Yahya](https://github.com/ayx234/)
- Frontend Mentor - [@ayx234](https://www.frontendmentor.io/profile/ayx234)
