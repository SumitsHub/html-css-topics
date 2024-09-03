# HTML Theory

## Table of contents
1.  Block-level Elements
2.  Inline Elements
3.  Semantic Elements

### 01. Block-level Elements

A block-level element always starts on a new line, and the browsers automatically add some space (a margin) before and after the element.

A block-level element always takes up the full width available (stretches out to the left and right as far as it can).

List of block-level elements:

```html
<address>   <article>   <aside> <blockquote>    <canvas>    <dd>    <div>   <dl>    <dt>    <fieldset>  <figcaption>    <figure>    <footer>    <form>  <h1>-<h6>   <header>    <hr>    <li>    <main>  <nav>   <noscript>  <ol>    <p> <pre>   <section>   <table> <tfoot> <ul>    <video>
```

### 02. Inline Elements

An inline element does not start on a new line.

An inline element only takes up as much width as necessary.

List of inline elements:
<a> <abbr> <acronym> <b><bdo> <big> <br> <button> <cite> <code> <dfn> <em> <i> <img> <input> <kbd> <label> <map> <object> <output> <q> <samp> <script> <select> <small> <span> <strong> <sub> <sup> <textarea> <time> <tt> <var>

Note: An inline element cannot contain a block-level element!

### 03. Semantic Elements

Semantic elements = elements with a meaning

A semantic element clearly describes its meaning to both the browser and the developer.

- Examples of non-semantic elements: <div> and <span> - Tells nothing about its content.
- Examples of semantic elements: <form>, <table>, and <article> - Clearly defines its content.

List of semantic elements:

<article> <aside>  <details> <figcaption> <figure> <footer> <header> <main>   <mark> <nav>    <section>   <summary>  <time>

Semantic elements with respective use: 
<header>: Contains the main heading of the page.
<nav>: Contains the navigation links.
<main>: Contains the main content of the page, including an <article>.
<aside>: Contains related information or secondary content.
<footer>: Contains the footer information.

#### Advantages of Semantic elements
1. Improved Accessibility
Semantic elements provide meaningful context to screen readers and other assistive technologies, making it easier for users with disabilities to navigate and understand the content.

2. Better SEO
Search engines can better understand the structure and content of a webpage when semantic elements are used, potentially improving the page's search engine ranking.

3. Enhanced Readability
Semantic elements make the HTML code more readable and maintainable for developers by clearly defining the purpose of different sections of the content.

4. Consistent Styling
Semantic elements allow for more consistent styling across different sections of a webpage, as they provide a clear structure that can be targeted with CSS.

5. Future-Proofing
Using semantic elements aligns with modern web standards, ensuring that the webpage remains compatible with future web technologies and browsers.