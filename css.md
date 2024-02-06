# CSS

## Getting started
CSS stands for Cascading Style Sheets. It's a style sheet language used to describe the presentation of a document written in a markup language like HTML. CSS describes how elements should be displayed on screen, in print, or in other media. It allows web developers to control the layout, colors, fonts, and other aspects of the presentation of their web pages, ensuring consistency and flexibility across different devices and screen sizes. CSS works by selecting HTML elements and applying styling rules to them, either directly within HTML files, through external CSS files, or via inline styling.

### 1. Selector
A CSS selector is a pattern used to select and style elements within an HTML document. Selectors target specific HTML elements based on their attributes, IDs, classes, or relationship to other elements. They allow you to apply styles to specific elements or groups of elements, giving you fine-grained control over the appearance of your web pages.

#### 1.1 Element selector
An element selector in CSS is used to target and apply styles to all elements of a specific type within an HTML document. It selects elements based solely on their HTML tag names.

Here's the basic syntax of an element selector:

```
element {
  /* CSS properties */
}
```

```
element {
  p {
    color: blue;
    font-size: 16px;
}
```
