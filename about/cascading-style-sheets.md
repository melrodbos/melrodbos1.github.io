## Reading CSS
- List of web pages and books utilized as reference to create this document:
  - [Treehouse blog](http://blog.teamtreehouse.com/getting-started-with-css-part-1)
  - [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
  - [Headway101](https://headway101.com/html-css-and-php-explained-an-introduction-to-internet-coding-basics/)
  - [Code Academy](http://www.codecademy.com/glossary/css/properties)
  - Book: **HTML & CSS Design and Build Websites** by John Duckett
- What is CSS? 
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
   - [`align-content:`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content)
    - Syntax: `align-content: center;`
   - [`background-color:`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
    - Syntax: `background-color: red;`
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
