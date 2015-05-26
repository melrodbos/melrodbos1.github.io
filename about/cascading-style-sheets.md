## Reading CSS
- List of web pages and books utilized as reference to create this document:
  - [Treehouse blog](http://blog.teamtreehouse.com/getting-started-with-css-part-1)
  - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
  - [Headway101](https://headway101.com/html-css-and-php-explained-an-introduction-to-internet-coding-basics/)
  - [Code Academy](http://www.codecademy.com/glossary/css/properties)
  - [CSS-Tricks](https://css-tricks.com/almanac/properties/a/align-content/)
  - Book: **HTML & CSS Design and Build Websites** by John Duckett
- **What is CSS?** 
  - CSS stands for *Cascading Style Sheets
  - Css styles the content of the page that HTML displays. In other words, with CSS we create rules to specify how content should be seen on a web page. 
  - A CSS rule consists of two parts: 
    1. **selector** 
      - Examples of selectors are *headers* (`h1`, `h2`, `h3`...), *paragraph* (`p`) and *body* (`body`).
      - Selectors *MATCH* HTML elements! 
      - They can contain one or more selectors (type, class or ID)
      - They are separated by *combinators*. Combinators explain the relationship between the selectors. Some examples include the use of *whitespace*, `>`, `+` and tilde `~`.

    2. **declaration**
  - The declaration will always sit inside the curly braces `{ }`.
  - It consists of a property name followed by a colon, which is then followed by a value. 
  - The following image from [Team Treehouse blog](http://blog.teamtreehouse.com/getting-started-with-css-part-1) shows a CSS rule:
  
  ![Alt text](http://blog.teamtreehouse.com/wp-content/uploads/2012/10/css-rule.jpg)

*Note: Each CSS rule can have as many properties as needed and each property will apply to the elements that the selector applies to.*

#### Properties
- What are properties?
  - Properties define the rendering of a document.
  - Properties will always have a value, even when its value is `none`.

##### Examples of properties:
   - [`align-content:`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content):This property is a sub-property of the [*Flexible Box Layout*](http://css-tricks.com/snippets/css/a-guide-to-flexbox/) module. It helps aligning a flex container's lines within it when there is extra space in the cross-axis. It is important to note that this property has no effect when the flexbox has only a single line.
  
    - Syntax: `align-content: center;`
    - Values: 
      - **flex-start**: Lines are packed starting from the cross-start. Cross-start edge of the first line and cross-start edge of the flex container are flushed together. Each following line is flush with the preceding.
      - **flex-end**: Lines are packed starting from the cross-end. Cross-end of the last line and cross-end of the flex container are flushed together. Each preceding line is flushed with the following line.
      - **center**: Lines are packed toward the center of the flex container. The lines are flushed with each other and aligned in the center of the flex container. Space between the cross-start edge of the flex container and first line and between cross-end of the flex container and the last line is the same.
      - **space-between**: Lines are evenly distributed in the flex container. The spacing is done such as the space between two adjacent items is the same. Cross-start edge and cross-end edge of the flex container are flushed with respectively first and last line edges.
      - **space-around**: Lines are evenly distributed so that the space between two adjacent lines is the same. The empty space before the first and after the last lines equals half of the space between two adjacent lines.
      - **stretch**: Lines stretch to use the remaining space. The free-space is split equally between all the lines.
            ![Alt text](http://www.w3.org/TR/css3-flexbox/images/align-content-example.svg) Image-[CSS Tricks](https://css-tricks.com/almanac/properties/a/align-content/)

   - [`background-color:`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    - Syntax: `background-color: red;`: This property sets the background color of an element, either through a color value or the keyword transparent.
    - Values:
      - **color**: It describes the uniform color of the background. Evan if one or several background-image properties are defined, this color can affect the rendering, by transparency if the images aren't opaque. *In CSS, the `transparent` value is a color.*
    
   - [`background-repeat:`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat)
    - Syntax: `background-repeat: repeat;`
    
   - [`background-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)
    - Syntax: `background-position: top;`
    
   - [`border-top-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-width)
    - Syntax: `border-top-width: 10em;` 
    
   - [`box-sizing`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)
    - Formal Syntax: `content-box | padding-box | border-box`
    
   - [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding)
    - Syntax: `padding: 1em;` 
    
   - [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin)
    - Syntax: `margin: 5% auto;` 
    
   - [`max-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height)
    - Syntax: `max-height: 3.5em;`
    
   - [`min-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height)
    - Syntax: `min-height: fit-content;`
    
   - [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)
    - Syntax: `font-size: xx-small;`
  
   - [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align)
    - Syntax: `text-align: justify-all;`
  
   - [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height)
    - Syntax: `line-height: normal;`
    
   - [`@media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media)

   - [`@font-face`](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face)
   
   - [`inherit`](https://developer.mozilla.org/en-US/docs/Web/CSS/inherit)
   
   - [`z-index`](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) 
   
   

#### Pseudo-elements
- [Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements) allow you to style certain parts of a document. 

##### All pseudo-elements:
  - [`::after (:after)`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after)
  - [`::before (:before)`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before)
  - [`::first-letter (:first-letter)`](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter)
  - [`::first-line (:first-line)`](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-line)
  - [`::selection`](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection)
  - [`::backdrop`](https://developer.mozilla.org/en-US/docs/Web/CSS/::backdrop)
