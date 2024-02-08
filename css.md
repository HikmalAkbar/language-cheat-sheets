# CSS 🤫🧏‍♂️

## Getting started
CSS stands for Cascading Style Sheets. It's a style sheet language used to describe the presentation of a document written in a markup language like HTML. CSS describes how elements should be displayed on screen, in print, or in other media. It allows web developers to control the layout, colors, fonts, and other aspects of the presentation of their web pages, ensuring consistency and flexibility across different devices and screen sizes. CSS works by selecting HTML elements and applying styling rules to them, either directly within HTML files, through external CSS files, or via inline styling.

### 1. Selector
A CSS selector is a pattern used to select and style elements within an HTML document. Selectors target specific HTML elements based on their attributes, IDs, classes, or relationship to other elements. They allow you to apply styles to specific elements or groups of elements, giving you fine-grained control over the appearance of your web pages.

#### 1.1 - Universal selector

> [!NOTE]
> Used for CSS reset.

The universal selector (*) in CSS matches any element type. It is often used to apply styles globally to all elements within a document. 

Here's the basic syntax of the universal selector:

```css
/*CSS Reset*/
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

#### 1.2 - Element selector

> [!NOTE]
> Used sometimes.

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

#### 1.3 - Class selector

> [!NOTE]
> Most used in project.

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

#### 1.4 - ID selector

> [!NOTE]
> Not good practice; refrain from using it.

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

> [!TIP]
> Website for contrast checker [Coolors.co](https://coolors.co/)

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

### 3. Units

> [!NOTE]
> Don't use *font-size: px;* as it is going to take away user's option from changing their browser font size 

In CSS, there are various units of measurement used to define sizes and distances. These units can be broadly categorized into two types: absolute units and relative units. Here's an overview of each:

3.1 - **Absolute Units**:
   - Pixel (px): A pixel is a single dot on a screen. It's a fixed-size unit that does not change with the size of the viewport. Pixels are commonly used for precise control over element sizes and positions.
   - Point (pt): A point is a physical unit of measurement commonly used in print design. One point is equal to 1/72 of an inch. It's less commonly used in web design but can be useful for maintaining consistent sizing across different media.

> [!TIP]
> - Use width with percentage instead of vw as vw tends to cause horizontal scroll to appear
> - Sometimes *min-height: 100vh;* might be used or not; [article](https://ilxanlar.medium.com/you-shouldnt-rely-on-css-100vh-and-here-s-why-1b4721e74487)

3.2 - **Relative Units**:
   - Percentage (%): Percentage units are relative to the parent element. For example, if you set an element's width to 50%, it will take up half the width of its parent element.
   - Viewport Width (vw): One viewport width unit is equal to 1% of the width of the viewport. This unit is useful for creating designs that scale with the size of the viewport.
   - Viewport Height (vh): One viewport height unit is equal to 1% of the height of the viewport. Similar to vw, vh is useful for creating designs that scale with viewport height.
   - Font-relative Lengths (em, rem): These units are relative to the font size of the element. em is relative to the font size of the parent element, while rem is relative to the font size of the root (html) element. They're commonly used for responsive typography.

### 4. Box Models
The CSS box model is a fundamental concept that describes how elements are rendered on a web page. It consists of four main components: content, padding, border, and margin. These components surround an element's content area and determine its size and spacing within the layout. Here's an overview of each component:

#### 4.1 - Content
This is the innermost part of the box and contains the actual content of the element, such as text, images, or other HTML elements. The content area's dimensions are specified using the width and height properties.

#### 4.2 - Padding
The padding is the space between the content area and the element's border. It's used to create space around the content without affecting the element's background or border. Padding can be specified using the padding property or individual properties like padding-top, padding-right, padding-bottom, and padding-left.

#### 4.3 - Border
The border surrounds the padding and content areas and defines the visible boundary of the element. It can have a thickness, style, and color specified using the border property or individual properties like border-width, border-style, and border-color.

#### 4.4 - Margin
The margin is the space outside the element's border and defines the distance between the element and adjacent elements in the layout. Margins can be specified using the margin property or individual properties like margin-top, margin-right, margin-bottom, and margin-left.

> [!TIP]
> - You can customize 4-sides of margin/padding

```css
.container {
    margin:  1em 2em; /*Margin top and bottom = 1em, while margin left and right = 2em*/
    padding: 1em 2m 3em; /*Padding top 1em, padding bottom = 2em, while padding left and right = 3em*/
}
```
