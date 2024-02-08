# CSS 🤫🧏‍♂️

## Getting started
CSS stands for Cascading Style Sheets. It's a style sheet language used to describe the presentation of a document written in a markup language like HTML. CSS describes how elements should be displayed on screen, in print, or in other media. It allows web developers to control the layout, colors, fonts, and other aspects of the presentation of their web pages, ensuring consistency and flexibility across different devices and screen sizes. CSS works by selecting HTML elements and applying styling rules to them, either directly within HTML files, through external CSS files, or via inline styling.

### 1. Selector
A CSS selector is a pattern used to select and style elements within an HTML document. Selectors target specific HTML elements based on their attributes, IDs, classes, or relationship to other elements. They allow you to apply styles to specific elements or groups of elements, giving you fine-grained control over the appearance of your web pages.

#### 1.1 - Universal selector - Only once / Very rare
The universal selector (*) in CSS matches any element type. It is often used to apply styles globally to all elements within a document. 

Here's the basic syntax of the universal selector:

```css
* {
    /* CSS properties */
}
```

```css
* {
    margin: 0;
    padding: 0;
}
```

#### 1.2 - Element selector - Sometimes
An element selector in CSS is used to target and apply styles to all elements of a specific type within an HTML document. It selects elements based solely on their HTML tag names.

Here's the basic syntax of an element selector:

```css
element {
  /* CSS properties */
}
```

```css
p {
    color: blue;
    font-size: 16px;
}
```

```css
html {
    margin: 0;
    padding: 0;
}
```

```css
main {
    margin: 0;
    padding: 0;
}
```

```css
body {
    margin: 0;
    padding: 0;
}
```

#### 1.3 - Class selector - Most used
A class selector in CSS is used to target and apply styles to elements that have a specific class attribute. Class selectors allow you to apply styles to multiple elements across your HTML document, even if they are different types of elements.

Here's the basic syntax of a class selector:

```css
.classname {
    /* CSS properties */
}
```

```css
.highlight {
    background-color: yellow;
    font-weight: bold;
}
```

```html
<p class="highlight">This paragraph has the highlight class.</p>
<div class="highlight">This div also has the highlight class.</div>
```

#### 1.4 - ID selector - Not good practice
An ID selector in CSS is used to target and apply styles to a single element with a specific ID attribute within an HTML document. IDs must be unique within a page, meaning only one element can have a particular ID at a time.

Here's the basic syntax of an ID selector:

```css
#idname {
    /* CSS properties */
}
```

```css
#header {
    background-color: gray;
    font-size: 20px;
}
```

```html
<div id="header">This is the header</div>
```

### 2. Colors
In CSS, colors can be specified using various formats, including predefined color names, hexadecimal notation, RGB values, RGBA values, HSL values, and HSLA values. Here's an overview of each format:

#### 2.1 - Predefined Color Names
CSS provides a set of predefined color names that you can use. For example:

```css
color: red;
background-color: blue;
```

#### 2.2 - Hexadecimal Notation
 Colors can also be specified using hexadecimal notation, which represents the red, green, and blue components of the color. Hexadecimal colors start with a hash (#) followed by three or six hexadecimal digits. For example:
 
```css
color: #ff0000; /* red */
background-color: #0000ff; /* blue */
```

#### 2.3 - RGB Values
RGB stands for red, green, and blue. Each color component is represented by an integer value between 0 and 255. RGB colors are specified using the rgb() function. For example:

```css
color: rgb(255, 0, 0); /* red */
background-color: rgb(0, 0, 255); /* blue */
```

#### 2.4 - RGBA Values
RGBA is similar to RGB, but with an additional alpha channel that represents the opacity of the color. The alpha value is specified as a number between 0 and 1. RGBA colors are specified using the rgba() function. For example:

```css
color: rgba(255, 0, 0, 0.5); /* semi-transparent red */
background-color: rgba(0, 0, 255, 0.75); /* semi-transparent blue */
```

#### 2.5 - HSL Values
HSL stands for hue, saturation, and lightness. Hue is represented as an angle between 0 and 360 degrees, saturation and lightness are represented as percentages. HSL colors are specified using the hsl() function. For example:
```css
color: hsla(0, 100%, 50%, 0.5); /* semi-transparent red */
background-color: hsla(240, 100%, 50%, 0.75); /* semi-transparent blue */
```

#### 2.6 - Predefined Color Names
HSLA is similar to HSL, but with an additional alpha channel for opacity. HSLA colors are specified using the hsla() function. For example:

```css
color: hsla(0, 100%, 50%, 0.5); /* semi-transparent red */
background-color: hsla(240, 100%, 50%, 0.75); /* semi-transparent blue */
```

#### 2.X Website for contrast checker

```
https://coolors.co/
```
