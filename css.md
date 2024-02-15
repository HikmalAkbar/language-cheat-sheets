
## Getting started
CSS stands for Cascading Style Sheets. It's a style sheet language used to describe the presentation of a document written in a markup language like HTML. CSS describes how elements should be displayed on screen, in print, or in other media. It allows web developers to control the layout, colors, fonts, and other aspects of the presentation of their web pages, ensuring consistency and flexibility across different devices and screen sizes. CSS works by selecting HTML elements and applying styling rules to them, either directly within HTML files, through external CSS files, or via inline styling.

> [!IMPORTANT]
> Documentation: [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)

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
> - Don't use *font-size: px;* as it is going to take away user's option from changing their browser font size.
> - Value keywords not included below: *normal, number, initial, inherit* 

In CSS, there are various units of measurement used to define sizes and distances. These units can be broadly categorized into two types: absolute units and relative units. Here's an overview of each:

3.1 - **Absolute Units (Length)**:
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

> [!TIP]
> - You can customize size and style each sides of border
> - You can use shorthand property

```css
.element {
    border-width: 2px;
    border-style: solid;
    border-color: red;
}
```

```css
.element {
    border: 2px solid red;
}
```

#### 4.4 - Margin
The margin is the space outside the element's border and defines the distance between the element and adjacent elements in the layout. Margins can be specified using the margin property or individual properties like margin-top, margin-right, margin-bottom, and margin-left.

> [!TIP]
> - You can customize each sides of margin/padding, order; top, right, bottom, left

```css
.container {
    margin:  1em 2em; /*Margin top and bottom = 1em, while margin left and right = 2em*/
    padding: 1em 2m 3em; /*Padding top 1em, padding right and left = 2em, while padding bottom = 3em*/
}
```

### 5. Typography
Typography in CSS refers to the styling and formatting of text on web pages. CSS provides various properties to control typography, including font-family, font-size, font-weight, line-height, text-align, and text-decoration, among others. Here's an overview of some commonly used typography-related CSS properties:

#### 5.1 Font Family
Specifies the font or list of fonts to be used for text rendering. You can specify multiple fonts separated by commas to provide fallback options if the preferred font is not available.

```css
body {
    font-family: Arial, sans-serif;
}
```

#### 5.2  Font Size
Sets the size of the font. You can specify the size in various units such as pixels (px), points (pt), percentages (%), ems (em), or keywords like small, medium, large, etc.

```css
p {
    font-size: 16px; /* Sets the font size to 16 pixels */
}

h1 {
    font-size: 2em; /* Sets the font size to twice the size of the parent element's font size */
}

span {
    font-size: 120%; /* Sets the font size to 120% of the parent element's font size */
}
```

#### 5.3 Font Style
The font-style property in CSS is used to specify the style of the font in text elements. It controls whether the text is displayed in a normal, italic, or oblique style.

```css
p {
    font-style: italic; /* Displays text in italic style */
}

h1 {
    font-style: normal; /* Resets text to normal (non-italic) style */
}
```

#### 5.4 Font Weight
Specifies the thickness of the font. Common values include normal, bold, bolder, lighter, or numeric values like 100, 200, ..., 900.

```css
p {
    font-weight: normal; /* Sets the text to normal thickness */
}

h1 {
    font-weight: bold; /* Sets the text to bold */
}

span {
    font-weight: 600; /* Sets the text to a font weight equivalent to "semi-bold" */
}
```

#### 5.5 Line Height
Sets the height of a line of text. It can be specified as a number, unitless value, percentage, or length.

```css
p {
    line-height: 1.5; /* Sets the line height to one and a half times the font size */
}

h1 {
    line-height: 1.2em; /* Sets the line height to 1.2 times the font size in pixels */
}

span {
    line-height: 120%; /* Sets the line height to 120% of the font size */
}
```

#### 5.6 Text Align
Specifies the horizontal alignment of text within its container. Common values include left, right, center, and justify.

```css
.container {
    text-align: center;
}
```

#### 5.7 Text Decoration
Adds decorative styling to text, such as underline, overline, line-through, or none.

```css
a {
    text-decoration: none;
}
```

#### 5.8 Text Indent
Used to specify the indentation of the first line of text within an element. It allows you to control the amount of space between the left (or right, in RTL languages) edge of the element's content area and the start of the text.

```css
p {
    text-indent: 2em;
    /*text-indent: 20px;
    text-indent: 25%;
    text-indent: -10px;*/
}
```

#### 5.9 Letter Spacing 
In CSS, the letter-spacing property is used to control the spacing between characters in text. It allows you to adjust the amount of space between each letter in a text element, either increasing or decreasing the spacing.

```css
p {
    letter-spacing: 2px; /* Increases the spacing between characters by 2 pixels */
}

h1 {
    letter-spacing: -0.1em; /* Decreases the spacing between characters by 0.1 em units */
}
```

#### 5.10 Word Spacing 
In CSS, the word-spacing property is used to control the spacing between words in text. It allows you to adjust the amount of space between words within a text element.

```css
p {
    word-spacing: 2px; /* Increases the spacing between words by 2 pixels */
}

h1 {
    word-spacing: -0.1em; /* Decreases the spacing between words by 0.1 em units */
}
```

#### 5.11 Text Transform 
The text-transform property in CSS is used to specify how the text should be capitalized. It allows you to control the capitalization of text within an element, converting it to uppercase, lowercase, or capitalize the first letter of each word.

```css
p {
    text-transform: uppercase; /* Converts text to uppercase */
}

h1 {
    text-transform: lowercase; /* Converts text to lowercase */
}

span {
    text-transform: capitalize; /* Capitalizes the first character of each word */
}
```

#### 5.12 White Space 
In CSS, the white-space property is used to control how white space inside an element is handled. It specifies whether to preserve white space characters such as spaces, tabs, and line breaks, or to collapse them into a single space.

```css
p {
    white-space: nowrap; /* Prevents text from wrapping */
}

pre {
    white-space: pre; /* Preserves white space characters exactly as they appear */
}

span {
    white-space: pre-wrap; /* Preserves white space characters and allows text to wrap */
}
```

#### 5.13 Text Overflow 
In CSS, the text-overflow property is used to specify how overflowed text should be handled when it's too long to fit within its container. It is particularly useful when dealing with text elements that have a fixed width and may contain content that exceeds that width.

```css
div {
    width: 200px; /* Set a fixed width for the container */
    white-space: nowrap; /* Prevent text from wrapping */
    overflow: hidden; /* Hide any overflowing content */
    text-overflow: ellipsis; /* Append an ellipsis to the end of the text */
}
```

### 6. Pseudo-classes
In CSS, pseudo-classes are used to define a special state of an element. They allow you to style elements based on user interaction or specific conditions that cannot be targeted using regular class or ID selectors alone.

Here are some commonly used pseudo-classes in CSS:

1. ***:hover***: Styles an element when the mouse pointer is over it.
2. ***:active***: Styles an element while it is being activated by the user (e.g., clicking a link).
3. ***:focus***: Styles an element when it gains focus (e.g., via keyboard navigation or clicking).
4. ***:visited***: Styles a link that has been visited by the user.
5. ***:first-child***: Styles the first child element of its parent.
6. ***:last-child***: Styles the last child element of its parent.
7. ***:nth-child()***: Styles elements based on their position within their parent. It allows you to target elements by index or using a formula.
8. ***:nth-of-type()***: Similar to :nth-child(), but only matches elements of a specified type.
9. ***:not()***: Styles elements that do not match a specified selector.
10. ***:checked***: Styles form elements (like checkboxes or radio buttons) that are checked.

```css
/* Styles for links */
a:hover {
    color: red; /* Change color when hovered */
}

/* Styles for form inputs */
input:focus {
    border-color: blue; /* Change border color when focused */
}

/* Styles for list items */
li:nth-child(odd) {
    background-color: lightgray; /* Alternating background colors for odd list items */
}
```

### 7. Display
In CSS, the display property specifies the display behavior of an element. It determines how an element is rendered in the document flow. There are several values for the display property, each with its own behavior. Here's a brief overview:

#### 7.1 Block
This value makes the element a block-level element. Block-level elements start on a new line and take up the full width available. Examples of block-level elements include <div>, <p>, <h1> - <h6>, <ul>, <ol>, etc.

```css
.example {
    display: block;
}
```

#### 7.2 Inline
This value makes the element an inline-level element. Inline-level elements do not start on a new line and only take up as much width as necessary. Examples of inline-level elements include <span>, <a>, <strong>, <em>, etc.

```css
.example {
    display: inline;
}
```

#### 7.3 Inline-block
This value makes the element an inline-level block container. It behaves like an inline-level element, but you can set a width, height, margins, and padding. It also respects line breaks and whitespace in the HTML.

```css
.example {
    display: inline-block;
}
```

#### 7.4 None
This value hides the element from the page layout entirely. The element will not be displayed and will not take up any space.

```css
.example {
    display: none;
}
```

