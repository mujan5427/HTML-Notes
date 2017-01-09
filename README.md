## Table of Contents

[Introduction](#introduction)

[Elements](#elements)

[Attributes](#attributes)

[Comments](#comments)

[Block and Inline Elements](#block-and-inline-elements)

[Entities](#entities)

[Uniform Resource Locators](#uniform-resource-locators)

[DOM](#dom)

[BOM](#bom)

[APIs](#apis)

[Reference Information](#reference-information)

<br />

## Introduction

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

<a name="html-browsers"></a>
Web Browsers

  * The purpose of a web browser (Chrome, IE, Firefox, Safari) is to read HTML documents and display them.

  * The browser does not display the HTML tags, but uses them to determine how to display the document.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

<a name="html-page-structure"></a>
HTML Page Structure

  * All HTML documents must start with a document type declaration：`<!DOCTYPE html>`.

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

## Comments

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

## APIs

Geolocation

  * The HTML Geolocation API is used to get the geographical position of a user.

  * Since this can compromise privacy, the position is not available unless the user approves it.

**[⬆ back to top](#table-of-contents)**

<br />
<br />

Local Storage

  * With local storage, web applications can store data locally within the user's browser.

  * Before HTML5, application data had to be stored in cookies, included in every server request. Local storage is   more secure, and large amounts of data can be stored locally, without affecting website performance.

  * Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the   server.

  * Local storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.

  * Local storage provides two objects for storing data on the client：

    - **window.localStorage** - stores data with no expiration date
    - **window.sessionStorage** - stores data for one session (data is lost when the browser tab is closed)

**[⬆ back to top](#table-of-contents)**

<br />
<br />

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

## Reference Information

HTML Tutorial (Website：[w3schools](http://www.w3schools.com/html/default.asp))

How Browsers Work: Behind the scenes of modern web browsers (Author：Tali Garsiel、Paul Irish)

Anatomy of an HTML element (Website：[Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics#Anatomy_of_an_HTML_element))

<br />
