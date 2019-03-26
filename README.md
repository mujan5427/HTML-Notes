## Table of Contents

[Introduction](#introduction)

  1. [HTML Tags](#html-tags)
  2. [Web Browsers](#web-browsers)
  3. [HTML Page Structure](#html-page-structure)
  4. [How HTML Elements Should Be Displayed](#how-html-elements-should-be-displayed)
  5. [Makes HTML Pages More Dynamic And Interactive By Javascript](#makes-html-pages-more-dynamic-and-interactive-by-javascript)

[Elements](#elements)

  1. [HTML Elements](#html-elements)
  2. [Nested HTML Elements](#nested-html-elements)
  3. [Do Not Forget The End Tag](#do-not-forget-the-end-tag)
  4. [Empty HTML Elements](#empty-html-elements)
  5. [Use Lowercase Tags](#use-lowercase-tags)

[Attributes](#attributes)

  1. [HTML Attributes](#html-attributes)
  2. [Use Lowercase Attributes](#use-lowercase-attributes)
  3. [Quote Attribute Values](#quote-attribute-values)
  4. [Single Or Double Quotes](#single-or-double-quotes)
  5. [Global Attributes](#global-attributes)
  6. [data-* Attribute](#data-attribute)

[Comments](#comments)

  1. [HTML Comment](#html-comment)
  2. [Conditional Comments](#conditional-comments)

[Block and Inline Elements](#block-and-inline-elements)

  1. [Block Level Elements](#block-level-elements)
  2. [Inline Elements](#inline-elements)

[Entities](#entities)

  1. [HTML Entities](#html-entities)
  2. [Non Breaking Space](#non-breaking-space)

[Uniform Resource Locators](#uniform-resource-locators)

  1. [HTML URL](#html-url)
  2. [URL Encoding](#url-encoding)

[HTML DOM](#html-dom)

  1. [What is HTML DOM](#what-is-html-dom)
  2. [DOM Methods](#dom-methods)
  3. [DOM Document](#dom-document)
  4. [DOM Events](#dom-events)
  5. [DOM Event Listener](#dom-event-listener)
  6. [DOM Nodes](#dom-nodes)
  7. [DOM Node Relationships](#dom-node-relationships)
  8. [DOM Node List](#dom-node-list)

[BOM](#bom)

  1. [What is BOM](#what-is-bom)
  2. [The Window Object](#the-window-object)
  3. [Window Screen Object](#window-screen-object)
  4. [Window Location Object](#window-location-object)
  5. [Window History Object](#window-history-object)
  6. [Window Navigator Object](#window-navigator-object)
  7. [Popup Boxes](#popup-boxes)
  8. [Timing Events](#timing-events)
  9. [Cookies](#cookies)

[APIs](#apis)

  1. [Geolocation](#geolocation)
  2. [Web Storage](#web-storage)
  3. [Web Worker](#web-worker)

[Performance](#performance)

  1. [Delay JavaScript Loading](#delay-javascript-loading)

[HTML Reference](#html-reference)

  1. [script](#script)

[Reference Information](#reference-information)

<br />

## Introduction

<a name="what-is-html"></a>
What is HTML ?

  * HTML is the standard markup language for creating Web pages.

    - HTML stands for Hyper Text Markup Language
    - HTML describes the structure of Web pages using markup
    - HTML elements are the building blocks of HTML pages
    - HTML elements are represented by tags
    - HTML tags label pieces of content such as "heading", "paragraph", "table", and so on
    - Browsers do not display the HTML tags, but use them to render the content of the page

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="html-versions"></a>
HTML versions

  * Since the early days of the web, there have been many versions of HTML：

    <table>
      <tr>
        <th width="300px">Version</td>
        <th width="50%">Year</td>
      </tr>
      <tr>
        <td>HTML</td>
        <td>1991</td>
      </tr>
      <tr>
        <td>HTML 2.0</td>
        <td>1995</td>
      </tr>
      <tr>
        <td>HTML 3.2</td>
        <td>1997</td>
      </tr>
      <tr>
        <td>HTML 4.01</td>
        <td>1999</td>
      </tr>
      <tr>
        <td>XHTML</td>
        <td>2000</td>
      </tr>
      <tr>
        <td>HTML 5</td>
        <td>2014</td>
      </tr>
    </table>

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="html-tags"></a>
HTML Tags

  * HTML tags are element names surrounded by angle brackets：

    ![This image is from MDN](https://mdn.mozillademos.org/files/9347/grumpy-cat-small.png)

    - HTML tags normally come in pairs like `<p>` and `</p>`
    - The first tag in a pair is the start tag, the second tag is the end tag
    - The end tag is written like the start tag, but with a forward slash inserted before the tag name
    - The start tag is also called the **opening tag**, and the end tag the **closing tag**.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="web-browsers"></a>
Web Browsers

  * The purpose of a web browser (Chrome, IE, Firefox, Safari) is to read HTML documents and display them.

  * The browser does not display the HTML tags, but uses them to determine how to display the document.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="html-page-structure"></a>
HTML Page Structure

  * All HTML documents must start with a document type declaration：`<!DOCTYPE html>`.

    > The <!DOCTYPE> declaration is not an HTML tag; it is an instruction to the web browser about what version of HTML the page is written in.

    > The <!DOCTYPE> declaration is NOT case sensitive.

  * The HTML document itself begins with `<html>` and ends with `</html>`.

  * The visible part of the HTML document is between `<body>` and `</body>`.

  * Below is an HTML page structure：

    ```html
    <!DOCTYPE html>
    <html>

      <head>
        <title>Page Title</title>
      </head>

      <body>

        <h1>My First Heading</h1>
        <p>My first paragraph.</p>

      </body>

    </html>
    ```

    > Only the content inside the `<body>` section (the white area above) is displayed in a browser.

  * Example Explained

    - The `<!DOCTYPE html>` declaration defines this document to be HTML5
    - The `<html>` element is the root element of an HTML page
    - The `<head>` element contains meta information about the document
    - The `<title>` element specifies a title for the document
    - The `<body>` element contains the visible page content
    - The `<h1>` element defines a large heading
    - The `<p>` element defines a paragraph

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="how-html-elements-should-be-displayed"></a>
How HTML elements should be displayed ?

  * Styling HTML with CSS

  * CSS is a language that describes the style of an HTML document.

  * CSS describes how HTML elements should be displayed.

  * CSS saves a lot of work. It can control the layout of multiple web pages all at once.

  * CSS can be added to HTML elements in 3 ways：

    - Inline - by using the style attribute in HTML elements

      ```html
      <h1 style="color:blue;">This is a Blue Heading</h1>
      ```

    - Internal - by using a `<style>` element in the `<head>` section

      ```html
      <!DOCTYPE html>
      <html>

        <head>

          <style>

            body {background-color: powderblue;}
            h1   {color: blue;}
            p    {color: red;}

          </style>

        </head>

        <body>

          <h1>This is a heading</h1>
          <p>This is a paragraph.</p>

        </body>

      </html>
      ```

    - External - by using an external CSS file

      ```html
      <!DOCTYPE html>
      <html>

        <head>
          <link rel="stylesheet" href="styles.css">
        </head>

        <body>

          <h1>This is a heading</h1>
          <p>This is a paragraph.</p>

        </body>

      </html>
      ```

  * The most common way to add CSS, is to keep the styles in separate CSS files.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="makes-html-pages-more-dynamic-and-interactive-by-javascript"></a>
Makes HTML pages more dynamic and interactive by JavaScript

  * The `<script>` tag is used to define a client-side script (JavaScript).

  * The `<script>` element either contains scripting statements, or it points to an external script file through the src attribute.

  * Common uses for JavaScript are image manipulation, form validation, and dynamic changes of content.

    > This JavaScript example writes "Hello JavaScript!" into an HTML element with id="demo"：

    ```html
    <script>
      document.getElementById('demo').innerHTML = 'Hello JavaScript!';
    </script>
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Elements

<a name="html-elements"></a>
HTML Elements

  * An HTML element usually consists of a start tag and end tag, with the content inserted in between.

  * The HTML element is everything from the start tag to the end tag.

  * HTML elements with no content are called **empty elements**. Empty elements do not have an end tag, such as the `<br>` element (which indicates a line break).

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="nested-html-elements"></a>
Nested HTML Elements

  * HTML elements can be nested (elements can contain elements).

  * All HTML documents consist of nested HTML elements.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="do-not-forget-the-end-tag"></a>
Do Not Forget the End Tag

  * Some HTML elements will display correctly, even if you forget the end tag：

    ```html
    <html>
      <body>

        <p>This is a paragraph
        <p>This is a paragraph

      </body>
    </html>
    ```
  * The example above works in all browsers, because the closing tag is considered optional.

  > Never rely on this. It might produce unexpected results and/or errors if you forget the end tag.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="empty-html-elements"></a>
Empty HTML Elements

  * HTML elements with no content are called empty elements.

  * `<br>` is an empty element without a closing tag (the `<br>` tag defines a line break).

  * Empty elements can be "closed" in the opening tag like this：`<br />`.

  * HTML5 does not require empty elements to be closed. But if you want stricter validation, or if you need to make your document readable by XML parsers, you must close all HTML elements properly.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="use-lowercase-tags"></a>
Use Lowercase Tags

  * HTML tags are not case sensitive：`<P>` means the same as `<p>`.

  * The HTML5 standard does not require lowercase tags, but W3C **recommends** lowercase in HTML, and demands lowercase for stricter document types like XHTML.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Attributes

<a name="html-attributes"></a>
HTML Attributes

  * All HTML elements can have attributes.

  * Attributes provide additional information about an element.

  * Attributes are always specified in the start tag.

  * Attributes usually come in name/value pairs like：name="value".

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="use-lowercase-attributes"></a>
Use Lowercase Attributes

  * The HTML5 standard does not require lowercase attribute names.

  * The title attribute can be written with uppercase or lowercase like Title and/or TITLE.

  * W3C recommends lowercase in HTML, and demands lowercase for stricter document types like XHTML.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="quote-attribute-values"></a>
Quote Attribute Values

  * The HTML5 standard does not require quotes around attribute values.

    ```html
    <a href=http://www.w3schools.com>
    ```

  * W3C **recommends** quotes in HTML, and demands quotes for stricter document types like XHTML.

  * Sometimes it is necessary to use quotes. This example will not display the title attribute correctly, because it contains a space：

    ```html
    <p title=About W3Schools>
    ```

    > Using quotes are the most common. Omitting quotes can produce errors.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="single-or-double-quotes"></a>
Single or Double Quotes ?

  * Double quotes around attribute values are the most common in HTML, but single quotes can also be used.

  * In some situations, when the attribute value itself contains double quotes, it is necessary to use single   quotes：

  ```html
  <p title='John "ShotGun" Nelson'>
  ```

  Or vice versa：

  ```html
  <p title="John 'ShotGun' Nelson">
  ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="global-attributes"></a>
Global Attributes

  * [The global attributes](http://www.w3schools.com/tags/ref_standardattributes.asp) can be used on **any** HTML element, such as `id`、`class` and `style`.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="data-attribute"></a>
data-* Attribute

  * The `data-*` attributes is a **global attribute** used to store custom data private to the page or application.

  * The `data-*` attributes gives us the ability to embed custom data attributes on all HTML elements.

  * The stored (custom) data can then be used in the page's JavaScript to create a more engaging user experience (without any Ajax calls or server-side database queries).

  * The `data-*` attributes consist of two parts：
    1. The attribute name should not contain any uppercase letters, and must be at least one character long after the prefix "data-".

    2. The attribute value can be any string.

  * The `*` may be replaced by any name following [the production rule of xml names](https://www.w3.org/TR/REC-xml/#NT-Name) with the following restrictions：

    * the name must not start with xml, whatever case is used for these letters.

    * the name must not contain any semicolon (`U+003A`).

    * the name must not contain capital `A` to `Z` letters.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Comments

<a name="html-comment"></a>
HTML Comment

  * Comment tags are used to insert comments in the HTML source code.

  * You can add comments to your HTML source by using the following syntax：

    ```html
    <!-- Write your comments here -->
    ```

  * There is an exclamation point `(!)` in the opening tag, but not in the closing tag.

  * Comments are not displayed by the browser, but they can help document your HTML source code.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="conditional-comments"></a>
Conditional Comments

  * You might stumble upon conditional comments in HTML：

    ```html
    <!--[if IE 9]>
        .... some HTML here ....
    <![endif]-->
    ```

  * Conditional comments defines some HTML tags to be executed by Internet Explorer only.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Block and Inline Elements

  > Every HTML element has a default display value depending on what type of element it is. The default display value for most elements is block or inline.

  > [Seeing examples of block-level and inline element on W3Schools](http://www.w3schools.com/html/html_blocks.asp)

<a name="block-level-elements"></a>
Block-level Elements

  * A block-level element always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).

  * Some examples of block-level elements：

    - `<div>`
    - `<h1> - <h6>`
    - `<p>`
    - `<form>`

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="inline-elements"></a>
Inline Elements

  * An inline element does not start on a new line and only takes up as much width as necessary.

  * Some Examples of inline elements：

    - `<span>`
    - `<a>`
    - `<img>`

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Entities

<a name="html-entities"></a>
HTML Entities

  * Reserved characters in HTML must be replaced with character entities.

  * If you use the less than (`<`) or greater than (`>`) signs in your text, the browser might mix them with tags.

  * Characters that are not present on your keyboard can also be replaced by entities.

  * To display a less than sign (`<`) we must write：`&lt;` or `&#60;`

    ```
    &entity_name;

    OR

    &#entity_number;
    ```

    > Advantage of using an entity name：An entity name is easy to remember.

    > Disadvantage of using an entity name： Browsers may not support all entity names, but the support for numbers is good.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="non-breaking-space"></a>
Non-breaking Space

  * Another common use of the non-breaking space is to prevent that browsers truncate spaces in HTML pages.

  * If you write 10 spaces in your text, the browser will remove 9 of them. To add real spaces to your text, you can use the `&nbsp;` character entity.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Uniform Resource Locators

<a name="html-url"></a>
HTML URL

  * A URL is another word for a web address.

  * A URL can be composed of words (w3schools.com), or an Internet Protocol (IP) address (192.68.20.50).

  * Web browsers request pages from web servers by using a URL.

  * A Uniform Resource Locator (URL) is used to address a document (or other data) on the web.

  * A web address, like http://www.w3schools.com/html/default.asp follows these syntax rules：

   ```
   scheme://prefix.domain:port/path/filename
   ```
   Explanation：

   - **scheme** - defines the type of Internet service (most common is http or https)
   - **prefix** - defines a domain prefix (default for http is www)
   - **domain** - defines the Internet domain name (like w3schools.com)
   - **port** - defines the port number at the host (default for http is 80)
   - **path** - defines a path at the server (If omitted: the root directory of the site)
   - **filename** - defines the name of a document or resource

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="urlencoding"></a>
URL Encoding

  * URLs can only be sent over the Internet using the ASCII character-set. If a URL contains characters outsid the ASCII set, the URL has to be converted.

  * URL encoding converts non-ASCII characters into a format that can be transmitted over the Internet.

  * URL encoding replaces non-ASCII characters with a `%` followed by hexadecimal digits.

  * URLs cannot contain spaces. URL encoding normally replaces a space with a plus (`+`) sign, or `%20`.

  * Your browser will encode input, according to the character-set used in your page.

  * The default character-set in HTML5 is UTF-8.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## HTML DOM

<a name="what-is-html-dom"></a>
What is HTML DOM ?

  * The DOM is a W3C (World Wide Web Consortium) standard.

  * The W3C DOM standard is separated into 3 different parts

    - Core DOM - standard model for all document types
    - XML DOM - standard model for XML documents
    - HTML DOM - standard model for HTML documents

      > We will dive into HTML DOM in following content

  * When a web page is loaded, the browser creates a Document Object Model (_DOM_) of the page.

  * The HTML DOM model is constructed as a tree of Objects：

    ![The HTML DOM Tree of Objects](http://www.w3schools.com/js/pic_htmltree.gif)

  * With the object model, JavaScript gets all the power it needs to create dynamic HTML：

    - JavaScript can change all the HTML elements in the page
    - JavaScript can change all the HTML attributes in the page
    - JavaScript can change all the CSS styles in the page
    - JavaScript can remove existing HTML elements and attributes
    - JavaScript can add new HTML elements and attributes
    - JavaScript can react to all existing HTML events in the page
    - JavaScript can create new HTML events in the page

  * The HTML DOM is a standard object model and programming interface for HTML. It defines：

    - The HTML elements as objects
    - The properties of all HTML elements
    - The methods to access all HTML elements
    - The events for all HTML elements

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-methods"></a>
DOM Methods

  * The HTML DOM can be accessed with JavaScript (and with other programming languages).

  * In the DOM, all HTML elements are defined as **objects**.

  * The programming interface is the properties and methods of each object.

  * A **property** is a value that you can get or set (like changing the content of an HTML element).

  * A **method** is an action you can do (like add or deleting an HTML element).

    ```html
    <html>
    <body>

    <p id="demo"></p>

    <script>
    document.getElementById("demo").innerHTML = "Hello World!";
    </script>

    </body>
    </html>
    ```

    > In the example above, getElementById is a **method**, while innerHTML is a **property**.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-document"></a>
DOM Document

  * The HTML DOM document object is the owner of all other objects in your web page.

  * The document object represents your web page.

  * If you want to access any element in an HTML page, you always start with accessing the document object.

    - **document.getElementById(id)**	- Find an element by element id
    - **document.getElementsByTagName(name)**	- Find elements by tag name
    - **document.getElementsByClassName(name)**	- Find elements by class name

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-events"></a>
DOM Events

  * A JavaScript can be executed when an event occurs, like when a user clicks on an HTML element.

  * To execute code when a user clicks on an element, add JavaScript code to an HTML event attribute：

    ```html
    <!DOCTYPE html>
    <html>
    <body>

    <h1 onclick="this.innerHTML = 'Ooops!'">Click on this text!</h1>

    </body>
    </html>
    ```

  * To assign events to HTML elements you can use event attributes.

    ```html
    <button onclick="displayDate()">Try it</button>
    ```

    > In the example above, a function named displayDate will be executed when the button is clicked.

  * The HTML DOM allows you to assign events to HTML elements using JavaScript：

    ```html
    <script>
    document.getElementById("myBtn").onclick = displayDate;
    </script>
    ```

    > In the example above, a function named _displayDate_ is assigned to an HTML element with the id="myBtn".

    > The function will be executed when the button is clicked.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-event-listener"></a>
DOM EventListener

  * The addEventListener() method attaches an event handler to the specified element.

  * The addEventListener() method attaches an event handler to an element without overwriting existing event handlers.

  * You can add many event handlers to one element.

  * You can add many event handlers of the same type to one element, i.e two "click" events.

  * You can add event listeners to any DOM object not only HTML elements. i.e the window object.

  * The addEventListener() method makes it easier to control how the event reacts to bubbling.

  * When using the addEventListener() method, the JavaScript is separated from the HTML markup, for better readability and allows you to add event listeners even when you do not control the HTML markup.

  * You can easily remove an event listener by using the removeEventListener() method.

  * addEventListener method syntax：

    ```
    element.addEventListener(event, function, useCapture);
    ```

    - The first parameter is the type of the event (like "click" or "mousedown").

    - The second parameter is the function we want to call when the event occurs.

    - The third parameter is a boolean value specifying whether to use event bubbling or event capturing. This parameter is optional.

      > You don't use the "on" prefix for the event; use "click" instead of "onclick".

  * There are two ways of event propagation in the HTML DOM, **bubbling** and **capturing**.

  * Event propagation is a way of defining the element order when an event occurs. If you have a `<p>` element inside a `<div>` element, and the user clicks on the `<p>` element, which element's "click" event should be handled first?

  * In bubbling the inner most element's event is handled first and then the outer： the `<p>` element's click event is handled first, then the `<div>` element's click event.

  * In capturing the outer most element's event is handled first and then the inner： the `<div>` element's click event will be handled first, then the `<p>` element's click event.

  * With the addEventListener() method you can specify the propagation type by using the `useCapture` parameter

  * The default value is false, which will use the bubbling propagation, when the value is set to true, the event uses the capturing propagation.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-nodes"></a>
DOM Nodes

  * According to the W3C HTML DOM standard, everything in an HTML document is a node：

    - The entire document is a document node
    - Every HTML element is an element node
    - The text inside HTML elements are text nodes
    - Every HTML attribute is an attribute node
    - All comments are comment nodes

  ![DOM HTML tree](http://www.w3schools.com/js/pic_htmltree.gif)

  * With the HTML DOM, all nodes in the node tree can be accessed by JavaScript.

  * New nodes can be created, and all nodes can be modified or deleted.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-node-relationships"></a>
DOM Node Relationships

  * The nodes in the node tree have a hierarchical relationship to each other.

  * The terms parent, child, and sibling are used to describe the relationships.

    - In a node tree, the top node is called the root (or root node)
    - Every node has exactly one parent, except the root (which has no parent)
    - A node can have a number of children
    - Siblings (brothers or sisters) are nodes with the same parent

      ```html
      <html>

        <head>
            <title>DOM Tutorial</title>
        </head>

        <body>
            <h1>DOM Lesson one</h1>
            <p>Hello world!</p>
        </body>

      </html>
      ```

      ![node tree](http://www.w3schools.com/js/pic_navigate.gif)

  * You can use the following node properties to navigate between nodes with JavaScript：

    - parentNode
    - childNodes[nodenumber]
    - firstChild
    - lastChild
    - nextSibling
    - previousSibling

    ex：

      ```html
      <title id="demo">DOM Tutorial</title>
      ```

      > The element node `<title>` (in the example above) does not contain text. It contains a text node with the value "DOM Tutorial".

      > Accessing the innerHTML property is the same as accessing the nodeValue of the first child：

      ```javascript
      var myTitle = document.getElementById("demo").firstChild.nodeValue;
      ```

      OR

      > Accessing the first child can also be done like this：

      ```javascript
      var myTitle = document.getElementById("demo").childNodes[0].nodeValue;
      ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="dom-node-list"></a>
DOM Node List

  * The getElementsByTagName() method returns a node list. A node list is an array-like collection of nodes.

  * The following code selects all `<p>` nodes in a document：

    ```javascript
    var myNodelist = document.getElementsByTagName("p");
    ```

  * The nodes can be accessed by an index number. To access the second `<p>` node you can write：

    ```javascript
    var y = myNodelist[1];
    ```

  * The length property defines the number of nodes in a node list：

    ```javascript
    var myNodelist = document.getElementsByTagName("p");

    var nodeListLength = myNodelist.length;
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## BOM

<a name="what-is-bom"></a>
What is BOM ?

  * Browser Object Model (_BOM_)

  * There are no official standards for the BOM.

  * Since modern browsers have implemented (almost) the same methods and properties for JavaScript interactivity, it is often referred to, as methods and properties of the BOM.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="the-window-object"></a>
The Window Object

  * The window object is supported by all browsers. It represents the browser's window.

  * All global JavaScript objects, functions, and variables automatically become members of the window object.

  * Global variables are properties of the window object.

  * Global functions are methods of the window object.

  * Even the document object (of the HTML DOM) is a property of the window object：

    ```javascript
    window.document.getElementById("header");
    ```

    is the same as：

    ```javascript
    document.getElementById("header");
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="window-screen-object"></a>
Window Screen Object

  * The window.screen object contains information about the user's screen.

  * The window.screen object can be written without the window prefix.

    Properties：

    - screen.width
    - screen.height
    - screen.availWidth
    - screen.availHeight
    - screen.colorDepth
    - screen.pixelDepth

    ex :

    ```javascript
    document.getElementById("demo").innerHTML = "Screen Width: " + screen.width;
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="window-location-object"></a>
Window Location Object

  * The window.location object can be used to get the current page address (URL) and to redirect the browser to a new page.

  * The window.location object can be written without the window prefix.

    Properties：

    - window.location.href - returns the href (_URL_) of the current page
    - window.location.hostname - returns the domain name of the web host
    - window.location.pathname - returns the path and filename of the current page
    - window.location.protocol - returns the web protocol used (http: or https:)
    - window.location.assign - loads a new document

    ex :

    ```javascript
    document.getElementById("demo").innerHTML = "Page location is " + window.location.href;
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="window-history-object"></a>
Window History Object

  * The window.history object contains the browsers history.

  * The window.history object can be written without the window prefix.

  * To protect the privacy of the users, there are limitations to how JavaScript can access this object.

    Some methods：

    - history.back() - same as clicking back in the browser
    - history.forward() - same as clicking forward in the browser

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="window-navigator-object"></a>
Window Navigator Object

  * The window.navigator object contains information about the visitor's browser.

  * The window.navigator object can be written without the window prefix.

    Some Properties：

    - navigator.appName
    - navigator.appCodeName
    - navigator.platform
    - navigator.cookieEnabled

    ex :

    ```javascript
    document.getElementById("demo").innerHTML = "cookiesEnabled is " + navigator.cookieEnabled;
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="popup-boxes"></a>
Popup Boxes

  * BOM has three kind of popup boxes：Alert box, Confirm box, and Prompt box.

  * those popup boxes can be written without the window prefix.

    Methods：

    - window.alert()
    - window.confirm()
    - window.prompt()

    ex :

    ```javascript
    alert("I am an alert box!");
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="timing-events"></a>
Timing Events

  * The window object allows execution of code at specified time intervals.

  * These time intervals are called timing events.

  * The two key methods to use with JavaScript are：

    - **setTimeout(function, milliseconds)**

      - Executes a function, after waiting a specified number of milliseconds.

    - **setInterval(function, milliseconds)**

      - Same as setTimeout(), but repeats the execution of the function continuously.

    ex :

    ```html
    <button onclick="setTimeout(myFunction, 3000)">Try it</button>

    <script>
    function myFunction() {
        alert('Hello');
    }
    </script>
    ```

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="cookies"></a>
Cookies

  * Cookies let you store user information in web pages.

  * Cookies are data, stored in small text files, on your computer.

  * When a web server has sent a web page to a browser, the connection is shut down, and the server forgets everything about the user.

  * Cookies were invented to solve the problem "how to remember information about the user"：

  * When a user visits a web page, his name can be stored in a cookie.

  * Next time the user visits the page, the cookie "remembers" his name.

  * Cookies are saved in name-value pairs like：

    ```
    username = John Doe
    ```

  * When a browser requests a web page from a server, cookies belonging to the page is added to the request. This way the server gets the necessary data to "remember" information about users.

  * JavaScript can create, read, and delete cookies with the document.cookie property.

    ```javascript
    document.cookie = "username=John Doe; expires=Thu, 18 Dec 2013 12:00:00 UTC; path=/";
    ```

    > You can also add an expiry date (in UTC time). By default, the cookie is deleted when the browser is closed

    > With a path parameter, you can tell the browser what path the cookie belongs to. By default, the cookie belongs to the current page.

  * The document.cookie property looks like a normal text string. But it is not.

  * Even if you write a whole cookie string to document.cookie, when you read it out again, you can only see the name-value pair of it.

  * If you set a new cookie, older cookies are not overwritten. The new cookie is added to document.cookie, so if you read document.cookie again you will get something like：

    ```
    cookie1 = value; cookie2 = value;
    ```

  * If you want to find the value of one specified cookie, you must write a JavaScript function that searches for the cookie value in the cookie string.

  * The `Domain` and `Path` directives define the scope of the cookie.

  * If Domain is specified, then subdomains are always included.

    > For example, if `Domain=mozilla.org` is set, then cookies are included on subdomains like `developer.mozilla.org`.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## APIs

<a name="geolocation"></a>
Geolocation

  * The HTML Geolocation API is used to get the geographical position of a user.

  * Since this can compromise privacy, the position is not available unless the user approves it.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="web-storage"></a>
Web Storage

  * With web storage, web applications can store data locally within the user's browser.

  * Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.

  * Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.

  * Web storage is per origin (per `domain` and `protocol`). All pages, from one origin, can store and access the same data.

  * Web storage provides two objects for storing data on the client：

    - **window.localStorage** - stores data with no expiration date
    - **window.sessionStorage** - stores data for one session (data is lost when the browser tab is closed)

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="web-worker"></a>
Web Worker

  > When executing scripts in an HTML page, the page becomes unresponsive until the script is finished.

  * A web worker is a JavaScript that runs in the background, independently of other scripts, without affecting the performance of the page. You can continue to do whatever you want: clicking, selecting things, etc., while the web worker runs in the background.

  * Since web workers are in external files, they do not have access to the following JavaScript objects：

    - The **window** object
    - The **document** object
    - The **parent** object

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Performance

<a name="delay-javascript-loading"></a>
Delay JavaScript Loading

  * Putting your scripts at the bottom of the page body lets the browser load the page first.

  * While a script is downloading, the browser will not start any other downloads. In addition all parsing and rendering activity might be blocked.

  > The HTTP specification defines that browsers should not download more than two components in parallel.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## HTML Reference

<a name="script"></a>
&lt;script&gt;

  * `async` attribute : If the async attribute is present, then the script will be fetched in parallel to parsing and evaluated as soon as it is available (potentially before parsing completes).

  * `defer` attribute : If the defer attribute is present, then the script will be fetched in parallel and evaluated when the page has finished parsing.

  ![](https://html.spec.whatwg.org/images/asyncdefer.svg)

**[⬆ back to top](#table-of-contents)**

<br />
<br />

## Reference Information

HTML Tutorial (Website：[w3schools](http://www.w3schools.com/html/default.asp))

How Browsers Work: Behind the scenes of modern web browsers (Author：Tali Garsiel、Paul Irish)

Anatomy of an HTML element (Website：[Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics#Anatomy_of_an_HTML_element))

Scripting (Website : [WHATWG HTML Living Standard](https://html.spec.whatwg.org/multipage/scripting.html#scripting-3))

<br />
