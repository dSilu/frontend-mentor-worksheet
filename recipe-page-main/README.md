# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the recipe page depending on their device's screen size
- See hover and focus states for interactive elements (if applicable)
- View accurate typography, structured nutrition tables, and balanced spacing mirroring the design preview

### Screenshot

![](./design/Screenshot.png)

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/your-solution-link](https://www.frontendmentor.io/solutions/your-solution-link)
- Live Site URL: [https://your-github-username.github.io/recipe-page/](https://your-github-username.github.io/recipe-page/)

## My process

### Built with

- Semantic HTML5 markup (`<main>`, `<section>`, `<table>`, `<ol>`, `<ul>`)
- CSS custom properties (variables)
- Custom local `@font-face` declarations (`Young Serif` and `Outfit`)
- CSS Table styling (`border-collapse`, column distribution)
- Flexbox for responsive card alignment
- Responsive design with CSS media queries

### What I learned

During this project, I tackled several nuanced layout and styling hurdles, particularly around semantic data tables, divider lines, typography imports, and list marker spacing.

#### 1. Nutrition Table Alignment & Clean Borders

Styling the nutrition values semantically using `<table>`, `<tr>`, and `<td>` required `border-collapse: collapse` to create crisp 1px divider lines between data rows, along with removing the border on the last row and setting column widths evenly:

```css
.nutrition-table {
  width: 100%;
  border-collapse: collapse;
}

.nutrition-table td {
  padding: 12px 16px;
  border-bottom: 1px solid hsl(30, 18%, 87%);
}

.nutrition-table td:first-child {
  width: 50%;
  color: hsl(30, 10%, 34%);
}

.nutrition-table td:last-child {
  color: hsl(14, 45%, 36%);
  font-weight: 700;
}

.nutrition-table tr:last-child td {
  border-bottom: none;
}
```

#### 2. Clean Horizontal Dividers

Instead of using default bevelled lines, I learned to reset `<hr>` tags completely to yield subtle separation between major recipe sections:

```CSS
hr {
  border: none;
  border-top: 1px solid hsl(30, 18%, 87%);
  margin: 30px 0;
}
```

#### 3. Styling List Numbers with ::marker

Styling only the ordered list numbers (giving them a bold weight and custom reddish-brown accent color without affecting the body text) was made simple with the `::marker` pseudo-element:

```CSS
ol li::marker {
  font-weight: 700;
  color: hsl(14, 45%, 36%);
}

ol li {
  padding-left: 12px;
  margin-bottom: 8px;
  line-height: 1.5;
}
```

### Continued development

- HTML Semantics for Data Displays: Deepening my understanding of when to use `<table>` vs definition lists (`<dl>`, `<dt>`, `<dd>`) for accessibility.

- CSS Counter Tricks: Practicing custom counters (counter-reset & counter-increment) to gain 100% control over numbered list alignment and multi-line wrapping.

- Fluid Typography: Exploring clamp() functions to smoothly scale typography between mobile and desktop viewport sizes.


### Useful resources

- MDN Web Docs - HTML Table Basics - Helped clarify table structure (`<tr>`, `<td>`, `<th>`) and how to collapse borders cleanly.

- MDN Web Docs - ::marker Pseudo-Element - Useful reference for styling bullet points and ordered list numbers without messy wrapper spans.

- CSS-Tricks: A Complete Guide to @font-face - Guided the configuration of local font files and variable weight ranges.

### AI Collaboration
Tools Used: AI Assistant (Gemini)

### Application:

- Consulted on semantic HTML choices between tables and definition lists for nutritional data.
- Debugged table column spacing and border-bottom styling.
- Resolved local @font-face path resolution and font-weight application.
- Explored list spacing options (padding-left vs CSS custom counters) to prevent multi-line instruction text from awkwardly wrapping beneath numbers.

**Takeaway**: Collaborating with AI helped quickly diagnose visual discrepancies between my implementation and the design spec, especially for CSS nuances like ::marker and border collapse.

### Author

- Frontend Mentor - [@dSilu](https://www.frontendmentor.io/profile/dSilu)
- GitHub - [@dSilu](https://github.com/dSilu)

### Acknowledgments

Thanks to Frontend Mentor for providing the realistic design challenge and starter assets!