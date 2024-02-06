# CSS

## Getting started
CSS stands for Cascading Style Sheets. It's a style sheet language used to describe the presentation of a document written in a markup language like HTML. CSS describes how elements should be displayed on screen, in print, or in other media. It allows web developers to control the layout, colors, fonts, and other aspects of the presentation of their web pages, ensuring consistency and flexibility across different devices and screen sizes. CSS works by selecting HTML elements and applying styling rules to them, either directly within HTML files, through external CSS files, or via inline styling.

### 1. Selector
A CSS selector is a pattern used to select and style elements within an HTML document. Selectors target specific HTML elements based on their attributes, IDs, classes, or relationship to other elements. They allow you to apply styles to specific elements or groups of elements, giving you fine-grained control over the appearance of your web pages.

#### 1.1 Element selector
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

#### 1.2 Class selector 
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

#### 1.3 ID selector - Not good practice
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

#### 2.1 Predefined Color Names
CSS provides a set of predefined color names that you can use. For example:
