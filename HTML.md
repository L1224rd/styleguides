### Filename

1. **Letters** MUST be all lowercase
	* e.g. `sidebar.html`
2. **Words** MUST be separated with a hyphen
	* e.g. `social-media-widget.html`
  
### Protocol

Use the HTTPS protocol for embedded resources where possible.

Always use the HTTPS protocol (https:) for images and other media files, style sheets, and scripts, unless the respective files are not available over HTTPS.

```
<!-- Not recommended: omits the protocol -->
<script src="//ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>

<!-- Not recommended: uses the HTTP protocol -->
<script src="http://ajax.googleapis.com/ajax/libs/jquery/3.1.0/jquery.min.js"></script>
```

### Document

This section showcases the main elements required in a complete HTML file.

1. **Doctype** MUST be specified and SHOULD be HTML5
	* e.g. `<!DOCTYPE html>`
2. **Language** MUST be defined in the `html` element
	* e.g. `<html lang="en">`
3. **Character encoding** MUST be defined as early as possible
	* e.g. `<meta charset="utf-8">`
4. **Viewport** MUST be included
	* e.g. `<meta name="viewport" content="width=device-width, user-scalable=no">`
5. **Head and body** elements MUST be included
	* e.g. `<head></head><body></body>`
  
### Comments

This section describes how comments should be formatted and used.

Use comments to:
- Explain something unconventional or not obvious.
- Divide the code into blocks

Do not use comments to:
- Comment code that is not being used

### 1. Single-line Comments

Single-line comments MUST be on one line and text inside MUST be surrounded by spaces.

#### &#10006; Incorrect

<pre lang=html>
&lt;!--
This is a comment
--&gt;
</pre>

&#8627; Incorrect because `<!--`, `This is a comment` and `-->` should be one line.

<pre lang=html>
&lt;!--This is a comment--&gt;
</pre>

&#8627; Incorrect because there is no space before or after `This is a comment`.

#### &#10004; Correct

<pre lang=html>
&lt;!-- This is a comment --&gt;
</pre>

<!-- ------------------------------ -->

### 2. Multi-line Comments

Multi-line comments MUST start and end on their own line and text MUST NOT be indented.

#### &#10006; Incorrect

<pre lang=html>
&lt;!-- This is a comment
that spans multiple lines
--&gt;
</pre>

&#8627; Incorrect because `<!--` and `This is a comment` are on one line.

<pre lang=html>
&lt;!--
	This is a comment
	that spans multiple lines
--&gt;
</pre>

&#8627; Incorrect because `This is a comment` and `that spans multiple lines` are indented.

#### &#10004; Correct

<pre lang=html>
&lt;!--
This is a comment
that spans multiple lines
--&gt;
</pre>

<!-- ------------------------------ -->

### 3. Closing Tag Comments

Closing tag comments SHOULD include the class or ID symbol and name.

#### &#10006; Incorrect

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot;&gt;
	...
&lt;/div&gt;&lt;!-- main-wrapper --&gt;
</pre>

&#8627; Incorrect because `#` prefix is missing.

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot;&gt;
	...
&lt;/div&gt;&lt;!-- .main-wrapper --&gt;
</pre>

&#8627; Incorrect because `main-wrapper` is prefixed with `.` instead of `#`.

#### &#10004; Correct

<pre lang=html>
&lt;div id=&quot;main-wrapper&quot;&gt;
	...
&lt;/div&gt;&lt;!-- #main-wrapper --&gt;
</pre>

### Indentation

Indent by 2 spaces at a time. You can set your vscode to indent with 2 spaces when you press tab.

e.g.

```
<ul>
  <li>Fantastic
  <li>Great
</ul>
```
```
.example {
  color: blue;
}
```

### Capitalization

Use only lowercase.
```
<!-- Not recommended -->
<A HREF="/">Home</A>
<!-- Recommended -->
<img src="google.png" alt="Google">
```
```
/* Not recommended */
color: #E5E5E5;
/* Recommended */
color: #e5e5e5;
```
### Quotes

When quoting attributes values, allways use double quotation marks.

### Class / Id names

- Put the section name before the class name/id if it is specific to that section.
- Use hyphen to separate words
- Avoid using to many words

Good

`<div id="servicos-carroussel-container">...</div>`

Bad

`<div id="Servicos_carroussel_title_content_container_div">...</div>`

### Semantic Elements

Many web sites contain HTML code like: `<div id="nav"> <div class="header"> <div id="footer">`
to indicate navigation, header, and footer. HTML5 offers new semantic elements to define different parts of a web page:

```
<aside>
<footer>
<header>
<main>
<mark>
<nav>
<section>
etc
```

Check this [w3schools guide](https://www.w3schools.com/html/html5_semantic_elements.asp) for more.
