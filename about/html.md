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
    1. [**HTML Elements**]( 
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
      
      - List of HTML block elements:
        - `<address>`: Contact information.
        - `<article> `: Article content.
        - `<aside>`: Aside content.
        - `<audio>`: Audio player.
        - `<blockquote>`: Long ("block") quotation.
        - `<canvas>`: Drawing canvas.
        - `<dd>`: Definition description.
        - `<div>`: Document division.
        - `<dl>`: Definition List.
        - `<fieldset>` Field set label.
        - `<figcaption>` HTML Figure caption.
        
    A. **Tags**
      - Tags are enclosed by angle brackets, and the closing tag begins with a forward slash.
      - Tags are labels that define and separate parts of your markup into elements.
      - Elements include two matching tags and everything in between. For example, the "<p>" element indicates a paragraph; the "<img>" element indicates an image.
      - There is *start* tag and a *closing* tag.
      - **Sintax**:
        - `<tag attribute='value'>content</tag keyword>`
      - Examples:
      ```
      <title> HTML Glossary </title>
      
      <em> I <strong>NEED</strong>to learn this!</em>
      ```
      
    B. **Attributes**
      - `*class`: 
      - `id`:
      - `href`:

    
  
