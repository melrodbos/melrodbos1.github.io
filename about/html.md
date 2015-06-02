## Reading HTML
- List of web pages and books utilized as reference to create this document:
  - [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML)
  - [I can build a Blog](http://icanbuildablog.com/2015/01/html-cheat-sheet-for-beginners/)
  - [Code Academy](http://www.codecademy.com/glossary/html)
  - Book: **HTML & CSS Design and Build Websites** by John Duckett
- What is HTML? 
  - HTML stands for **HyperText Markup Language**. 
  - The word markup was used by editors who marked up manuscripts (usually with a blue pencil) when giving instructions for revisions. 
  - "Markup" now means something slightly different: a language with specific syntax that instructs a Web browser how to display a page. Once again, HTML separates "content" (words, images, audio, video, and so on) from "presentation" (instructions for displaying each type of content).
  - HTML is used for creating and visually representing a webpage. It describes the structure of the page.
- HTML Structure:
- Image from *HTML & CSS Design and Build Websites* by John Duckett:
- ![Image of html structure](http://www.htmlandcssbook.com/images/sample-chapter/medium/dps-5.jpg)
    1. [**HTML Elements**](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) 
      - HTML uses a pre-defined set of elements to define content types. 
      - Elements contain one or more "tags" that contain or express content:
       ![Anatomy of an HTML Element](https://mdn.mozillademos.org/files/7659/anatomy-of-an-html-element.png)

      - [**Block-level elements**](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements)
        - A block-level element occupies the entire space of its parent element (container), thereby creating a "block."
      - HTML:
        ```
        <p>This paragraph is a block-level element; its background has been colored to display the paragraph's parent element.</p>
        ```
      - CSS:
      ```
      p { background-color: #8ABB55; }
      ```
      - Block-level elements may appear only within a <body> element.
      - By default, block-level elements begin on new lines.
      
      - **List of HTML block-level elements**:
        - `<address>`: Contact information.
        - `<article> `: Article content.
        - `<aside>`: Aside content.
        - `<audio>`: Audio player.
        - `<blockquote>`: Long ("block") quotation.
        - `<canvas>`: Drawing canvas.
        - `<dd>`: Definition description.
        - `<div>`: Document division.
        - `<dl>`: Definition List. 
          - Encloses a list of pairs of terms and descriptions. Common uses for this element are to implement a glossary or to display metadata.
          - Includes [global atributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes).
        - `<ol>`: Ordered list.
        - `<ul>`: Unordered list.
        - `<fieldset>` Field set label.
        - `<figcaption>` HTML Figure caption.
        - `<form>`: Input form.
        
      - **List of HTML elements**:
        - `<legend>`: The HTML <legend> Element (or HTML Legend Field Element) represents a caption for the content of its parent `<fieldset>`.
        - `<input>`: It is used to create interactive controls for web-based forms in order to accept data from the user. The semantics of an <input> varies considerably depending on the value of its type attribute.
        - `<label>`: The HTML Label Element (<label>) represents a caption for an item in a user interface. It can be associated with a control either by placing the control element inside the <label> element, or by using the for attribute. Such a control is called the labeled control of the label element.
        - `<button>`: It represents a clickable button.
        - `<select>`: It represents a control that presents a menu of options. The options within the menu are represented by `<option>` elements, which can be grouped by `<optgroup>` elements. 
        - `<textarea>`: It represents a multi-line plain-text editing control.
        - `<option>`: It is used to create a control representing an item within a `<select>`, an `<optgroup>` or a `<datalist>` HTML5 element.
        
#### Tags
>
      1. Tags are enclosed by angle brackets, and the closing tag begins with a forward slash.
      2. Tags are labels that define and separate parts of your markup into elements.
      3. Elements include two matching tags and everything in between. For example, the `<p>` element indicates a paragraph; the `<img>` element indicates an image.
      4. There is *start* tag and a *closing* tag.
>
- **Sintax**:
      - `<tag attribute='value'>content</tag keyword>`
    - Examples:

      ```
      <title> HTML Glossary </title>

      <em> I <strong>NEED</strong>to learn this!</em>
      ```

  - **Attributes**
    - Attributes include the additional inormation in a tag. 
    - They usually consist of 2 parts: `Name` and `Value`.

  - [**Global Attributes**](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes): 
    - `class`: Used with CSS to style elements with common properties.
    - `id`: Often used with CSS to style a specific element. Its value is unique, meaning that ids cannot be repeated in an html document.
    - `hidden`:
    - `title`: Contains a text representing advisory information related to the element it belongs to. 

* [x] **Reading HTML**
  * [ ] come to the `<table>`
  * [ ] no one ever reads the `<caption>`
  * [ ] `<col>` waiting? I got `<colgroup>`!
  * [ ] you've got a nice `<tbody>`
  * [ ] but don't let it go to your `<thead>`
  * [ ] shot in the `<tfoot>`
  * [ ] `<tr>` coffee?
  * [ ] `<td>` or not `<td>`?
  * [ ] that would be `<th>`


    
  
