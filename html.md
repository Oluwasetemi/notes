# HTML
 Table of Content
 -------
1. HTML Introduction
2. HTML Basics
3. HTML Attributes
4. HTML Advanced
5. HTML Entities
6. CSS in HTML - Cascading Style Sheets

objectives
-----
* Write simple HTML documents
* Write simple HTML Tags / Elements
* Understand the difference between closing and self closing tags
* Understand Block Element and Inline Elements
* Write HTML Tags with basic attributes
* Use multimedia tags like audio, video, images
* Write CSS inside HTML with the style attribute and the style tag

  

## HTML Introduction

HTML (Hypertext Markup Language) is the most basic building block of the Web. It describes and defines the content of a web page. Other technologies besides HTML are generally used to describe a web-page's appearance/presentation (CSS) or functionality/behavior (JavaScript).

  

HTML uses "markup" to annotate text, images, and other content for display in a Web browser. HTML markup includes special "elements" such as `<head>, <title>, <body>, <header>, <footer>, <article>, <section>, <p>, <div>, <span>, <img>`, and many others.

  

Tags in HTML are case insensitive. That is, they can be written in uppercase, lowercase, or a mixture. Example `<title>` tag can be written as `<Title>,</TiTlE>`or in any other way.

  

HTML Documents not html language. HTML document forms a web page and collection of web pages gives us a website.

  

The General Document Structure

  
```html
<!DOCTYPE html>
<html>
<head>
<!-- Document metadata -->
</head>
<body>
<!-- Document content -->
</body>
</html>
```
  

The General Rule

  
```html
<tagName> Some Content</tagName> <!-- Closing Tags -->

<tagName /> <!-- Self - Closing Tags -->
```
  

NB - Naming of files convention and folder structure arrangement will be worth paying attention to.

  

Example 1

Exercise 1 - Writing your first html page with the following tags

  

HTML Basics

Element or Tags

  
```html
<p>I am a paragraph<p>

<h1>I am a header</h1>

  

<h2>header 2 is slightly smaller to header 1</h2>

<h6> I'm the smallest header</h6>

<button>Click me!😀</button>

  

<ul>

<li>list 1</li>

<li>list 2</li>

</ul>

  

<img src="absolute/relative_path.png">

  

<a href="url">Click me</a>

<!-- I am a comment -->
```
  

HTML (Hypertext Markup Language) elements are usually either "block-level" elements or "inline" elements.

type:

block  - A block-level element occupies the entire space of its parent element (container), thereby creating a "block."

  

inline  - inline elements are those which only occupy the space bounded by the tags defining the element, instead of breaking the flow of the content. In this article, we'll examine HTML inline elements and how they differ from block-level elements.

  

HTML Attributes

Elements in HTML have attributes; these are additional values that configure the elements or adjust their behavior in various ways to meet the criteria the users want.

  
```html
<tagName attribute="attribute-value" single-Attribute > Some Content </tagName>
```
  

Global Attributes

`accesskey` - define a keyboard shortcut to activate or add focus to the element

`class` - Often used with CSS to style elements with common properties.

`contenteditable` - Indicates whether the element's content is editable.

`contextmenu` - Defines the ID of a <menu> element which will serve as the element's context menu.

`data-*` - Lets you attach custom attributes to an HTML element. Ex: data-test, data-name

`dir` - Defines the text direction. Allowed values are ltr (Left-To-Right) or rtl (Right-To-Left)

`draggable` - Defines whether the element can be dragged.

`dropzone` - Indicates that the element accept the dropping of content on it.

`hidden` - Indicates that the element accept the dropping of content on it.

`id` - Often used with CSS to style a specific element. The value of this attribute must be unique.

`lang` - Defines the language used in the element.

`style` - Defines CSS styles which will override styles previously set.

`tabindex` - Overrides the browser's default tab order and follows the one specified instead.

`title` - Text to be displayed in a tooltip when hovering over the element.

  

  

Element Special Attributes

|Attribute Name  | Elements |Description|
|--|--|--|
| row | table | |
| types="" | input |various types of input element |

Custom Attributes

Create with `data-*` global attributes

  

HTML Advanced

Grouping

* Base elements in HTML5 - The HTML elements that allow you to build the most basic web page

body - The container for a web page's content. Must be a direct child of `<html>`, and must be an ancestor of all HTML elements (except where noted). Type: Block,Closing

  
```html
<!DOCTYPE html>

<html>

<body>

<!-- Document content -->

</body>

</html>
```
  

`head` - Defines a container for a web page's metadata. Type: Block, Closing

  
```html
<!DOCTYPE html>

<html>

<head>

<!-- Document metadata -->

</head>

</html>
```
  

`html` - Defines the root element of an HTML document. All other elements must be contained within this root element. `:root` Type: Block. Closing

  
```html
<!DOCTYPE html>

<html>

</html>
```
  

`link` - Defines a link between the current web page and an external link or resource. Self closing

  
```html
<link rel="stylesheet" type="text/css" href="[https://htmlreference.io/css/website.css](https://htmlreference.io/css/website.css)">
````
  

`href` - Defines the URL of the link.

NB - Absolute and relative URL(Uniform Resource Locator)

`rel` - Defines a link type, explaining how the link relates to the current web page."stlesheet/icon/author/next"

`type` - Defines the type of the linked resource. "type/css"

  

`meta` - Defines metadata attached to a web page.

  
```html
<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">

<meta name="viewport" content="width=device-width, initial-scale=1">

<meta name="theme-color" content="#ffffff">

  

<!-- Refresh the page every 5 seconds -->

<meta http-equiv="refresh" content="5">

  

<!-- Redirect instantly to  [https://cssreference.io](https://cssreference.io/)  -->

<meta http-equiv="refresh" content="0; url=[https://cssreference.io](https://cssreference.io/)">
```
  

Other attributes

`charset` - Defines the character encoding for the whole web page. "UTF-8"

`http-equiv` - Defines meta rules for the web page. "Content-Security-Policy/refresh/X-UA-Compatible"

`name` - Defines additional information attached to the web page. "viewport/theme-color"

`content` - Defines the content of the metadata. This varies according to the name or http-equiv value.

"width=device-width, initial-scale=1"

  

`script` - Defines a container for an external script.

  
```html
<script src="[https://htmlreference.io/javascript/my-scripts.js](https://htmlreference.io/javascript/my-scripts.js)"></script>

  

<script type="text/javascript">

console.log('Hello World');

</script>
```
  

other Attributes

`src` - Defines the source of the external script.

`type` - Defines the MIME type of the external script.

("text/javascript").* This is for .js files.

`async` - Allows the external script to be loaded asynchronously.

  

HTML Forms

* `Form` - The HTML elements that allow you to build interactive forms

  

`button` - Defines a clickable button | inline | closing
```html
<button>

Submit form

</button>
```
  

attribute

`name`, `value`, `type`="submit|reset",

no value attribute

`disabled`

`autofocus`

  

`fieldset` - Defines a group of controls within a form | Block | Closing

  
```html
<form action="/subscribe" method="post">

<fieldset>

<legend>Subscribe to the Newsletter</legend>

<input type="email" name="email">

<button>Ok</button>

</fieldset>

</form>
```
attributes

`disabled`

  

`form` - defines an interactive form with controls | Block | Closing
```html
<form action="/signup" method="post">

<p>

<label>Title</label>

  

<label>

<input type="radio" name="title" value="mr">

Mr

</label>

<label>

<input type="radio" name="title" value="mrs">

Mrs

</label>

<label>

<input type="radio" name="title" value="miss">

Miss

</label>

</p>

<p>

<label>First name</label>

  

<input type="text" name="first_name">

</p>

<p>

<label>Last name</label>

  

<input type="text" name="last_name">

</p>

<p>

<label>Email</label>

  

<input type="email" name="email" required>

</p>

<p>

<label>Phone number</label>

  

<input type="tel" name="phone">

</p>

<p>

<label>Password</label>

  

<input type="password" name="password">

</p>

<p>

<label>Country</label>

  

<select>

<option>China</option>

<option>India</option>

<option>United States</option>

<option>Indonesia</option>

<option>Brazil</option>

</select>

</p>

<p>

<label>

<input type="checkbox" value="terms">

I agree to the <a href="/terms">terms and conditions</a>

</label>

</p>

<p>

<button>Sign up</button>

<button type="reset">Reset form</button>

</p>

</form>
```
  

attributes

`action` - define the url the form's information is sent to when submitted

`method` - define the HTTP method used when submitting the form

`name`

`autocomplete`

`target`="_blank || _self || _parent || _top"

`enctype`="application/x-www-form-urlencoded" || enctype="multipart/form-data" *input type file || enctype="text/plain"

no-value-attribute

`novalidate`

  

  

`input` - defines an interactive control within a web form. | inline | Self-closing

  
```html
<input type="text" name="first_name" placeholder="e.g. Alex">

type *Required text|email|number|checkbox|radio* link radio buttons through a similar name| submit | file
```
`name`

`placeholder`

best=practice: it is recommended to have a `label` to describe the input matching the `for` attribute of the `label` to the `id` of thee `input`  , and use the `placeholder` to showcase an example

no value attribute

`required`

`disabled`

  
```html
<label>

<input type="radio" name="newsletter" value="yes">

Yes

</label>

<label>

<input type="radio" name="newsletter" value="no">

No

</label>

<form>

<label>Email</label>

  

<input type="email" name="email" placeholder="e.g.  [alex@smith.com](mailto:alex@smith.com)">

</form>
```
  

`legend` - defines a caption for a parent's content.| Block | Closing

  
```html
<form action="/subscribe" method="post">

<fieldset>

<legend>Subscribe to the Newsletter</legend>

<input type="email" name="email">

<button>Ok</button>

</fieldset>

</form>
```
  

`textarea` - defines a multi-line text control within a web from. | inline| closing

  
```html
<textarea name="message">

</textarea>
```
Other Attributes

`name`

`autocomplete="on/off"`

`minlength="20"`

`maxlength="100"`

`placeholder="Enter a message"`

`cols="40"`

`rows="6"`

`wrap="hard/soft"`

no value attributes

`disabled`

`required`

`autofocus`

`readonly`

`spellcheck`

  

*Select

  

  

  

* `List` - The HTML elements that allow you to build all kinds of lists

  

`dd` - defines a data definition for term and it's list

`dl` - defines a definition list

`dt` - defines a definition term

  
```html
<dl>

<dt>Web</dt>

<dd>The part of the Internet that contains websites and web pages</dd>

<dt>HTML</dt>

<dd>A markup language for creating web pages</dd>

<dt>CSS</dt>

<dd>A technology to make HTML look better</dd>

</dl>
```
  

`li` - defines a list item within an ordered list `<ol> or unordered list <ul>`. Closing

  
```html
<ol>

<li>Step one</li>

<li>Step two</li>

<li>????</li>

<li>PROFIT!!!</li>

</ol>

<p>My shopping list:</p>

<ul>

<li>Milk</li>

<li>Bread</li>

<li>Chocolate</li>

<li>More chocolate</li>

</ul>
```
  

`ol` - define an ordered list. Block | Closing

  
```html
<ol>

<li>Step one</li>

<li>Step two</li>

<li>????</li>

<li>PROFIT!!!</li>

</ol>
```
attributes

`type="1"`. default uses numbers other include - "a", "A", "i", "I".

`start="3"`

reversed *no value is required

  

`ul` - define an un-ordered list. Block | Closing

  
```html
<p>My shopping list:</p>

<ul>

<li>Milk</li>

<li>Bread</li>

<li>Chocolate</li>

<li>More chocolate</li>

</ul>
```
  

HTML Tables

* Tables - The HTML elements that allow you to build tables

  

`captio`n - defines the title of a `<table>` | Block | Closing

  

`<caption>The Beatles</caption>`

  

`table` - defines a container for tabular data.|Block | Closing

  
```html
<table>

<thead>

<tr>

<th>Name</th>

<th>Instrument</th>

</tr>

</thead>

<tfoot>

<tr>

<th>Name</th>

<th>Instrument</th>

</tr>

</tfoot>

<tbody>

<tr>

<td>John Lennon</td>

<td>Rhythm Guitar</td>

</tr>

<tr>

<td>Paul McCartney</td>

<td>Bass</td>

</tr>

<tr>

<td>George Harrison</td>

<td>Lead Guitar</td>

</tr>

<tr>

<td>Ringo Starr</td>

<td>Drums</td>

</tr>

</tbody>

</table>
```
  

`tbody` - defines a group of table rows <tr>

  
```html
<tbody>

<tr>

<td>John Lennon</td>

<td>Rhythm Guitar</td>

</tr>

<tr>

<td>Paul McCartney</td>

<td>Bass</td>

</tr>

<tr>

<td>George Harrison</td>

<td>Lead Guitar</td>

</tr>

<tr>

<td>Ringo Starr</td>

<td>Drums</td>

</tr>

</tbody>
```
  

`td` - defines a table cell. Must be a direct child of a `<tr>`

  
```html
<tr>

<td>George Harrison</td>

<td>Lead Guitar</td>

</tr>
```
`colspan` - Defines how many columns a cell should span across. = "3" - You can use any integer.

`rowspan` - Defines how many rows a cell should span across. = "2" - You can use any integer.

  

`tfoot` - defines a group of table rows `<tr>` at the end of a `<table>

  
```html
<tfoot>

<tr>

<th>Name</th>

<th>Instrument</th>

</tr>

</tfoot>
```
  

`th` - defines a table header. Must be a direct child of a <tr>

  
```html
<th>Name</th>

<th>Instrument</th>
```
`colspan` - Defines how many columns a cell should span across. = "3" - You can use any integer.

`rowspan` - Defines how many rows a cell should span across. = "2" - You can use any integer.

  

`thead` - defines a group of table rows `<tr>` at the start of a `<table>`.

  
```html
<thead>

<tr>

<th>Name</th>

<th>Instrument</th>

</tr>

</thead>
```
  

`tr` - defines a table row

  ```html
<tr>

<td>George Harrison</td>

<td>Lead Guitar</td>

</tr>
```
Semantic Elements can be powered to behave like a table using the following tags with css display property

display: table /* `<table>` */

display: table-cell /* `<td>` */

display: table-row /* `<tr>` */

display: table-column /* `<col>` */

display: table-column-group /* `<colgroup`> */

display: table-footer-group /* `<tfoot>` */

display: table-header-group /* `<thead>` */

  

* `Semantic` - The HTML elements that allow you to structure your web page semantically

  

`article` - defines a self-contained block of content that can exit in any context. It can have its own header, footer, sections...etc. Useful for a list of blog posts | Block | Closing

  
```html
<article>

<header>

<h3>

<a href="/my-blog-post">My blog post</a>

</h3>

</header>

<section>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>

</section>

<footer>

<small>

Posted on <time datetime="2017-04-29T19:00">Apr 29</time> in <a href="/category/code">Code</a>

</small>

</footer>

</article>
```
`aside` - defines a block of content that is related to the main content. Displayed as a sidebar usually.| Block | Closing

  
```html
<main>

<h1>My blog post</h1>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>

<p>etc.</p>

</main>

<aside>

<h3>About the author</h3>

<p>Frontend Designer from Bordeaux, currently working for Improbable in sunny London.</p>

</aside>
```
  

  

`figcaption` - defines the caption of a `<figure>`. | Block | Closing

  
```html
<figure>

<img src="/images/html-reference-logo.png" alt="HTML Reference logo">

<figcaption>The HTML Reference logo</figcaption>

</figure>
```
  

`figure` - defines a single self-contained element, usually an image. | Block | Closing

  
```html
<figure>

<img src="/images/html-reference-logo.png" alt="HTML Reference logo">

</figure>
```
  

`footer` - defines the footer of a web page or section.

  
```html
<footer>

HTML Reference - A free reference to all HTML5 elements and attributes

</footer>
```
  

`header` - defines the header of a web page or section | Block | Closing

  
```html
<header>

<h1>HTML Reference</h1>

<nav>

<a>Home</a>

<a>About</a>

<a>Contact</a>

</nav>

</header>
```
  

`main` - defines the main content of a web page. Can be displayed with a sidebar | Block | Closing

  
```html
<main>

<h1>My blog post</h1>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>

<p>etc.</p>

</main>

<aside>

<h3>About the author</h3>

<p>Frontend Designer from Bordeaux, currently working for Improbable in sunny London.</p>

</aside>
```
  

`mark` - defines highlighted text | inline| Closing

  

We use HTML5 to write `<mark>content</mark>` on the Web.

  

`nav` - defines a section with a navigation links.| Blok | Closing

  
```html
<nav>

<a href="/">Home</a>

<a href="/about">About</a>

<a href="/contact">Contact</a>

</nav>
```
  

`section` - defines a section within a web page | Block | Closing

  
```html
<section>

<h2>Section title</h2>

<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec viverra nec nulla vitae mollis.</p>

</section>
```
  

  

`time` - defines a time on a 24hr clock.| inline| Closing

  

The game starts at `<time datetime="2017-04-29T19:00">19:00</time>.`

`datetime` - Defines the time and date. "2017-04-29T19:00" .The value needs to be a valid time string.

  

HTML Entities

An HTML entity is a piece of text ("string") that begins with an ampersand (&) and ends with a semicolon (;) . Entities are frequently used to display reserved characters (which would otherwise be interpreted as HTML code), and invisible characters (like non-breaking spaces). You can also use them in place of other characters that are difficult to type with a standard keyboard. Use any reference tool or decoder tool.

Character

Entity

Note

& - `&amp;`

Interpreted as the beginning of an entity or character reference.

< - `&lt;`

Interpreted as the beginning of a tag

\> -`&gt;`

Interpreted as the ending of a tag

" - `&quot;`

Interpreted as the beginning and end of an attribute's value.

  

CSS - Cascading Style Sheets

* inline Style using style global attribute

* using style tags `<style></style>`

Bonus - Hot module reloading && Emmet

https://browsersync.io/

*webpack or web-dev-server

parcel

  

```sh
browser-sync start --server --files "index.html, css/*.css, js/*.js" --index "index.html"
```
  

HTML Projects

Create a composition with html

Clone the HTML portion of any webpage

build from scratch any idea

Freecodecamp Projects

  

Slides

1. HTML Introduction

2. HTML Basic

3. Multimedia embedding

4. HTML tables

5. HTML forms

6. \* using HTML to solve common problems

7. HTML Advanced

8. CORS *enable image, settings attribute

9. FOCUS using DOM

10. using application cache

11. preload content with rel="preload"

  

HTML Reference

MDN

htmlreference.io

[Freecodecamp](https://guide.freecodecamp.org/html) -  [Attributes](https://guide.freecodecamp.org/html#attributes-panel),  [Elements](https://guide.freecodecamp.org/html#elements-panel)  and  [Tutorials](https://guide.freecodecamp.org/html#tutorials-panel)


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMjA2MDMyODQsLTkyMjg5MTY1MF19
-->
