## Table of Contents

[Introduction](#introduction)

[Elements](#elements)

[Attributes](#attributes)

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

  * All HTML documents must start with a document type declaration: `<!DOCTYPE html>`.

  * The HTML document itself begins with <html> and ends with </html>.

  * The visible part of the HTML document is between <body> and </body>.

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

## Reference Information

HTML Tutorial (Website：[w3schools](http://www.w3schools.com/html/default.asp))

How Browsers Work: Behind the scenes of modern web browsers (Author：Tali Garsiel、Paul Irish)

Anatomy of an HTML element (Website：[Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics#Anatomy_of_an_HTML_element))

<br />
