# Day 002

## CSS

### Introduction to CSS:

CSS (**Cascading Style Sheets**) is used to **style and design**
websites.\
Think of **HTML** as the skeleton, and **CSS** as the clothes and makeup
that make it attractive.

------------------------------------------------------------------------

## When to Use CSS?

-   **Inline CSS** → Quick fixes or testing (not recommended for large
    projects).\
-   **Internal CSS** → When styles are only for a **single page**.\
-   **External CSS** → Best practice; keeps styles separate, reusable,
    and scalable.

------------------------------------------------------------------------

## Types of CSS:

1.  **Inline CSS**
    -   Used when you want to style a **single element** only.\
    -   Example:

    ``` html
    <h1 style="color:blue;">This is a blue heading</h1>
    ```
2.  **Internal CSS**
    -   Useful for **small projects** or one-page websites.\
    -   Example:

    ``` html
    <head>
    <style>
    body {
      background-color: lightblue;
    }
    </style>
    </head>
    ```
3.  **External CSS**
    -   Best for **real-world projects**. Styles apply across multiple
        pages.\
    -   Example:

    ``` html
    <head>
    <link rel="stylesheet" href="styles.css">
    </head>
    ```

    ``` css
    /* styles.css */
    body {
      background-color: lightblue;
      font-size: 20px;
    }
    ```

------------------------------------------------------------------------

## When to Use What?

-   Use **inline CSS** only for **quick testing/debugging**.\
-   Use **internal CSS** for **single-page projects**.\
-   Use **external CSS** for **multi-page websites** and **team
    projects**.

------------------------------------------------------------------------

## Key CSS Concepts (With Use Cases):

### 1. Selectors

 1. Universal Selector
Apply style to **all elements**.

```css
* { margin: 0; padding: 0; box-sizing: border-box; }
```
👉 Mostly used for **reset** or **global rules**.

 2. Grouping Selector
Same styles for multiple elements.

```css
h1, h2, h3 { font-family: Arial, sans-serif; }
```
👉 Avoid repeating CSS.

 3. Descendant Selector (space ` `)
Target elements **inside another element**.

```css
div p { color: green; }
```
👉 Use when you want style only in a **specific container**.

 4. Child Selector (`>`)
Direct child only (not deeper levels).

```css
ul > li { list-style: none; }
```
👉 When you don’t want nested elements to be affected.

5. Adjacent Sibling Selector (`+`)
Target the element **immediately after** another.

```css
h1 + p { font-style: italic; }
```
👉 Good for styling text right after headings.

6. General Sibling Selector (`~`)
Target **all siblings after** an element.

```css
h1 ~ p { color: gray; }
```
👉 Useful when multiple siblings exist.

7. Attribute Selectors
Based on HTML attributes.

```css
input[type="text"] { border: 1px solid black; }
a[target="_blank"] { color: blue; }
```
👉 Great for **forms** and **links**.

8. Pseudo-classes
Special states of elements.

```css
a:hover { text-decoration: underline; }
input:focus { border-color: green; }
li:first-child { font-weight: bold; }
```
👉 Use for **interaction states**.

9. Pseudo-elements
Style parts of an element.

```css
p::first-line { font-size: 18px; }
p::before { content: "👉 "; }
```
👉 Adds decoration/content without changing HTML.

10. Combinators Mix

```css
nav ul li a:hover { color: red; }
```
👉 Powerful when combining multiple selectors.

💡 **Pro Tip:**
- Classes = Reusable styles ✅
- IDs = Rare, only unique elements 🚫
- Attribute + pseudo = Advanced targeting 🔥


------------------------------------------------------------------------

### 2. Colors

-   **Named colors, Hex, RGB, HSL** → Use based on project need.\
-   **RGBA** is best when you want **transparency**.

------------------------------------------------------------------------

### 3. Layouts

-   **Box model** → Use when adjusting spacing (margin, padding,
    border).\
-   **Flexbox** → Use for **one-dimensional layouts** (row or column).\
-   **Grid** → Use for **two-dimensional layouts** (rows and columns).

------------------------------------------------------------------------

### 4. Positioning

-   **Relative** → Nudge element slightly.\
-   **Absolute** → Place relative to parent.\
-   **Fixed** → Stick to viewport (good for navbars).\
-   **Sticky** → Sticks until scroll pushes it.

------------------------------------------------------------------------

### 5. Responsiveness

-   Use **media queries** to make websites mobile-friendly.

    ``` css
    @media (max-width: 600px) {
      body { background: lightgrey; }
    }
    ```

------------------------------------------------------------------------

### 6. Transitions & Animations

-   Use **transitions** for smooth hover effects.\
-   Use **animations** when you need continuous movement.

------------------------------------------------------------------------

### 7. Variables (CSS Custom Properties)

-   Use when you want consistent design values.

    ``` css
    :root {
      --main-color: blue;
    }
    h1 { color: var(--main-color); }
    ```

------------------------------------------------------------------------

### 8. SASS (Advanced)

-   Use for **nesting, variables, and mixins** → makes large projects
    easier to manage.

------------------------------------------------------------------------

## Best Practices (When to Use Them)

-   Always prefer **external CSS** in real projects.\
-   Use **classes** for styling, not IDs.\
-   Use **mobile-first approach** with media queries.\
-   Organize CSS in **modules** for big projects.

------------------------------------------------------------------------

🔥 CSS is the language of design. Start small, but always think about
**reusability, maintainability, and scalability**.
------------------------------------------------------------------------