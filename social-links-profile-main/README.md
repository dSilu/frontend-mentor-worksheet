# Frontend Mentor - Social links profile solution

This is a solution to the [Social links profile challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-links-profile-UG32l9m6dQ). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

## Overview

### The challenge

Users should be able to:

- See hover, focus, and active states for all interactive links on the page
- Navigate through all links seamlessly using only keyboard controls (`Tab`, `Shift + Tab`, `Enter`)

### Screenshot

![](./preview.jpg)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup (`<a>`, `<h1>`, `main`)
- CSS custom properties & HSL color values
- Flexbox for centralized component alignment
- Custom local typography via `@font-face`
- Mobile-first approach

### What I learned

During this challenge, I reinforced several key foundational concepts across CSS loading, box-model mechanics, and semantic web standards:

1. **Local Font Configuration & `font-display`**:
   
   Configured custom local font files properly with forward slashes and learned how `font-display: swap` prevents Flash of Invisible Text (FOIT) by displaying fallback text while downloading.

    ```css
    @font-face {
    font-family: 'Inter';
    src: url('./assets/fonts/Inter-VariableFont_slnt,wght.ttf') format('truetype');
    font-weight: 100 900;
    font-style: normal;
    font-display: swap;
    }

2. **Semantic Links vs. Buttons**:
    
    Used semantic `<a>` tags instead of `<button>` tags since the UI navigates to external URLs. Implemented secure anchor attributes alongside smooth interactive states.

    ```HTML
    <a href="[https://github.com](https://github.com)" class="link" target="_blank" rel="noopener noreferrer">GitHub</a>
    ```

3. **Box Sizing & Interactive Transitions**:

    Applied a global box-sizing: border-box reset to keep padding constrained within container widths, combined with transition states for mouse and keyboard navigation:

    ```CSS
    .link {
        display: block;
        width: 100%;
        padding: 14px 16px;
        background-color: hsl(0, 0%, 20%);
        color: hsl(0, 0%, 100%);
        text-decoration: none;
        border-radius: 8px;
        transition: background-color 0.2s ease, color 0.2s ease;
    }

    .link:hover,
    .link:focus-visible {
        background-color: hsl(75, 94%, 57%);
        color: hsl(0, 0%, 8%);
    }
    ```


### Continued development

- Fluid Typography & Units: Further exploring relative sizing using rem and em to make layouts accessible across varying browser preferences.
- Accessibility & Focus Management: Building deeper knowledge around :focus-visible patterns and ARIA roles for rich web applications.


### Useful resources

MDN Web Docs: Links vs Buttons - Clear explanation on when to use anchor tags versus standard button elements.


### AI Collaboration

- **Tools Used**: Gemini
- **Workflow**: Leveraged AI for real-time visual debugging, clarifying CSS units (rem vs px), understanding the role of font-display, and ensuring full keyboard accessibility compliance.
- **Takeaway**: Using AI as an interactive pair-programmer helped rapidly identify syntax oversights (such as path slash formatting and padding constraints) while explaining the underlying browser behavior.


### Author

- Frontend Mentor - [@dSilu](https://www.frontendmentor.io/profile/dSilu)
- GitHub - [@dSilu](https://github.com/dSilu)

