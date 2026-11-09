## 1. TAGS

Line numbers in the last column point to the full example page in [[Lines Used HTML]]. Concepts (elements, tags, block vs inline) are in [[HTML Basics]].

### Page structure

| #   | Tag                | Attribute                    | Use<br>[[Use of Tags]]                                                                                                             | Example                                              | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | ------------------ | ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | ----------------------------------------- |
| 1   | ==🟡`<!DOCTYPE>`== | N/A                          | Firstline of each HTML file, indicates what language the web page is supposed to expect.                                           | `<!DOCTYPE html>`                                    | 1                                         |
| 2   | `<html>`           | `lang`                       | Firstline after the DOCTYPE, all the code is supposed to happen between the two of these tags.                                     | `<html lang="en">`<br>something<br>here<br>`</html>` | 2                                         |
| 3   | `<head>`           | N/A                          | Holds information *about* the page (title, character set, CSS links). Nothing in it shows on the page.                             | `<head>`<br>`<title>SeeSolve</title>`<br>`</head>`   | 3                                         |
| 4   | `<meta>`           | `charset`, `name`, `content` | Gives the browser extra facts about the page: the character set, how to size the page on phones, a description for search engines. | `<meta charset="UTF-8">`                             | 4, 5, 6                                   |
| 5   | `<title>`          | N/A                          | The page name shown on the browser tab, in bookmarks and in search results.                                                        | `<title>SeeSolve</title>`                            | 7                                         |
| 6   | `<link>`           | `rel`, `href`                | Connects the page to another file, most often a CSS stylesheet or the tab icon.                                                    | `<link rel="stylesheet" href="main.css">`            | 8, 9                                      |
| 7   | `<style>`          | N/A                          | Lets you write CSS directly inside the HTML page.                                                                                  | `<style> p { color: teal; } </style>`                | 10                                        |
| 8   | `<script>`         | `src`, `type`, `defer`       | Adds JavaScript, either written inside it or loaded from a file with `src`.                                                        | `<script src="app.js"></script>`                     | 102                                       |
| 9   | `<body>`           | N/A                          | Holds everything the user actually sees on the page.                                                                               | `<body>`<br>`<h1>Hello</h1>`<br>`</body>`            | 14                                        |

### Page layout

| #   | Tag         | Attribute     | Use<br>[[Use of Tags]]                                                                             | Example                                    | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | ----------- | ------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------ | ----------------------------------------- |
| 10  | `<header>`  | N/A           | The top area of a page or section: logo, site name, menu.w w q q q q q                             | `<header><h1>SeeSolve</h1></header>`       | 16                                        |
| 11  | `<nav>`     | N/A           | Wraps the main navigation links (the menu).                                                        | `<nav><a href="#">Home</a></nav>`          | 18                                        |
| 12  | `<main>`    | N/A           | The main content of the page, different on every page.                                             | `<main id="app">...</main>`                | 27                                        |
| 13  | `<section>` | `id`          | Groups related content into a part of the page, usually with its own heading.                      | `<section id="courses">...</section>`      | 28, 39, 70, 84                            |
| 14  | `<article>` | N/A           | A self-contained piece that would make sense on its own, like a blog post, card or lesson.         | `<article><h3>Step by step</h3></article>` | 60                                        |
| 15  | `<aside>`   | N/A           | Side content related to the page but not the main point: tips, sidebars.                           | `<aside><p>Tip: ...</p></aside>`           | 94                                        |
| 16  | `<footer>`  | N/A           | The bottom area of a page or section: copyright, contact, credits.                                 | `<footer><p>&copy; 2026</p></footer>`      | 98                                        |
| 17  | `<div>`     | `class`, `id` | A general box for grouping things so CSS or JavaScript can target them. Has no meaning on its own. | `<div class="card">...</div>`              | 87                                        |
| 18  | `<span>`    | `class`, `id` | A general box for part of a line of text, so you can style or change just that part.               | `<span class="answer">x = 2</span>`        | 55                                        |

### Text

| #   | Tag | Attribute | Use<br>[[Use of Tags]] | Example | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | --- | --------- | ---------------------- | ------- | ----------------------------------------- |
| 19 | `<h1>` to `<h6>` | N/A | Headings, from most important (`<h1>`) to least (`<h6>`). | `<h1>Choose your course</h1>` | 29, 31, 40, 61 ... |
| 20 | `<p>` | N/A | A paragraph of text. | `<p>This is a paragraph.</p>` | 30, 55, 56, 66 ... |
| 21 | `<br>` | N/A | A line break inside text, like pressing Enter. | `Line one<br>Line two` | 56 |
| 22 | `<hr>` | N/A | A horizontal line that separates topics. | `<hr>` | 36 |
| 23 | `<strong>` | N/A | Marks important text. Shown in **bold**. | `<strong>Important</strong>` | 30 |
| 24 | `<em>` | N/A | Emphasis, like stressing a word when speaking. Shown in *italics*. | `<em>answers</em>` | 30 |
| 25 | `<sub>` / `<sup>` | N/A | Subscript (small, lowered) and superscript (small, raised) text. | `H<sub>2</sub>O`, `x<sup>2</sup>` | 56 |
| 26 | `<code>` | N/A | Shows a short piece of code in a monospace font. | `<code>let x = 5;</code>` | 63 |
| 27 | `<pre>` | N/A | Preformatted text: keeps every space and line break exactly as typed. | `<pre><code>...</code></pre>` | 63 |
| 28 | `<blockquote>` | `cite` | A longer quotation from another source, shown indented. | `<blockquote>Quote here</blockquote>` | 62 |
| 29 | `<!-- -->` | N/A | A comment: a note for people reading the code. The browser ignores it. | `<!-- Top of the page -->` | 15 |

### Links and media

| #   | Tag | Attribute | Use<br>[[Use of Tags]] | Example | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | --- | --------- | ---------------------- | ------- | ----------------------------------------- |
| 30 | `<a>` | `href`, `target` | A hyperlink to another page, a file, or a spot on the same page. | `<a href="https://mdn.io">MDN</a>` | 17, 20, 21, 22 |
| 31 | `<img>` | `src`, `alt`, `width`, `height` | Shows an image. | `<img src="logo.png" alt="SeeSolve logo">` | 17 |
| 32 | `<video>` | `src`, `controls`, `width` | Plays a video file. | `<video src="intro.mp4" controls></video>` | 88 |
| 33 | `<iframe>` | `src`, `title`, `width`, `height` | Embeds another web page inside yours, such as a YouTube video. | `<iframe src="https://www.youtube.com/embed/ID"></iframe>` | 89 |
| 34 | `<canvas>` | `id`, `width`, `height` | A blank drawing area that JavaScript can draw on: graphs, animations, games. | `<canvas id="graph" width="600" height="400"></canvas>` | 57 |

### Lists

| #   | Tag | Attribute | Use<br>[[Use of Tags]] | Example | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | --- | --------- | ---------------------- | ------- | ----------------------------------------- |
| 35 | `<ul>` | N/A | An unordered (bulleted) list. | `<ul><li>Item</li></ul>` | 19 |
| 36 | `<ol>` | `start`, `type` | An ordered (numbered) list. | `<ol><li>First</li></ol>` | 32 |
| 37 | `<li>` | N/A | One item in a `<ul>` or `<ol>`. | `<li>MCR3U: Functions</li>` | 20, 21, 22, 33 ... |

### Tables

| #   | Tag | Attribute | Use<br>[[Use of Tags]] | Example | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | --- | --------- | ---------------------- | ------- | ----------------------------------------- |
| 38 | `<table>` | N/A | A table of data in rows and columns. | `<table>...</table>` | 72 |
| 39 | `<tr>` | N/A | Table row. | `<tr><td>0</td><td>1000</td></tr>` | 73, 77 |
| 40 | `<th>` | `colspan`, `scope` | A header cell: the title of a column or row. Bold and centred by default. | `<th>Year</th>` | 74, 75 |
| 41 | `<td>` | `colspan`, `rowspan` | A normal data cell. | `<td>1000.00</td>` | 78, 79 |

### Forms and inputs

| #   | Tag | Attribute | Use<br>[[Use of Tags]] | Example | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | --- | --------- | ---------------------- | ------- | ----------------------------------------- |
| 42 | `<form>` | `action`, `method`, `id` | Groups inputs that are submitted together. | `<form id="solve-form">...</form>` | 41 |
| 43 | `<label>` | `for` | The text name for an input. | `<label for="problem">Problem</label>` | 42, 44, 49, 52 |
| 44 | `<input>` | `type`, `id`, `name`, `value`, `placeholder`, `min`, `max`, `step`, `required`, `checked` | A box or control the user fills in. `type` decides what kind. | `<input type="text" id="problem">` | 43, 50, 52 |
| 45 | `<button>` | `type`, `disabled` | A clickable button. | `<button type="submit">Solve</button>` | 53 |
| 46 | `<select>` | `id`, `name` | A drop-down menu. | `<select id="course">...</select>` | 45 |
| 47 | `<option>` | `value`, `selected` | One choice in a `<select>`. | `<option value="mcr3u">MCR3U</option>` | 46, 47 |
| 48 | `<textarea>` | `rows`, `cols`, `placeholder` | A big box for typing several lines of text. | `<textarea rows="4"></textarea>` | 86 |
| 49 | `<output>` | `for`, `id` | Shows the result of a calculation or a slider's value. | `<output id="a-value">1</output>` | 51 |

### Interactive

| #   | Tag | Attribute | Use<br>[[Use of Tags]] | Example | Common/ Used Lines<br>[[Lines Used HTML]] |
| --- | --- | --------- | ---------------------- | ------- | ----------------------------------------- |
| 50 | `<details>` / `<summary>` | `open` | A section that opens and closes when clicked, with no JavaScript needed. | `<details><summary>Hint</summary>...</details>` | 64 |

## 2. ATTRIBUTES

Attributes go inside the opening tag as `name="value"`. Some are true/false switches with no value, like `required`, `checked`, `disabled`, `controls`, `hidden`.

### Global attributes (work on any tag)

| #   | Attribute | Works on | What it does | Example |
| --- | --- | --- | --- | --- |
| 1 | `id` | Any tag | A unique name for one element. Used by CSS (`#name`), JavaScript and `#` links. Never repeat an id on a page. | `<main id="app">` |
| 2 | `class` | Any tag | A group name for styling many elements the same way (`.name` in CSS). One element can have several, separated by spaces. | `<span class="answer big">` |
| 3 | `style` | Any tag | CSS written directly on one element. Handy for quick tests; prefer a CSS file. | `<p style="color: red">` |
| 4 | `title` | Any tag | Extra info shown as a tooltip when you hover. | `<abbr title="Ontario">ON</abbr>` |
| 5 | `hidden` | Any tag | Hides the element. JavaScript can remove it to show the element again. | `<p hidden>Secret</p>` |
| 6 | `lang` | Any tag | Language of the content, usually set once on `<html>`. | `<html lang="en">` |
| 7 | `dir` | Any tag | Text direction: `ltr` or `rtl`. | `<p dir="rtl">` |
| 8 | `data-*` | Any tag | Your own custom info for JavaScript or CSS to read; you choose the name after `data-`. | `<li data-course="mcr3u">` |
| 9 | `tabindex` | Any tag | Controls whether the element can be reached with the Tab key (`0` = yes, `-1` = only by code). | `<div tabindex="0">` |
| 10 | `aria-label` | Any tag | A name for screen readers when there is no visible text, e.g. an icon button. | `<button aria-label="Close">X</button>` |

### Element-specific attributes

| #   | Attribute | Works on | What it does | Example |
| --- | --- | --- | --- | --- |
| 11 | `charset` | `<meta>` | Character set of the page. Always `UTF-8`. | `<meta charset="UTF-8">` |
| 12 | `name` / `content` | `<meta>` | A piece of page info and its value. | `<meta name="description" content="...">` |
| 13 | `rel` | `<link>`, `<a>` | How the linked file relates to the page (`stylesheet`, `icon`). | `<link rel="stylesheet" href="main.css">` |
| 14 | `href` | `<a>`, `<link>` | The address of the page or file. | `<a href="about.html">` |
| 15 | `target` | `<a>`, `<form>` | Where to open the link; `_blank` means a new tab. | `<a href="..." target="_blank">` |
| 16 | `src` | `<img>`, `<script>`, `<video>`, `<iframe>` | The file to load. | `<img src="logo.png">` |
| 17 | `alt` | `<img>` | Text description of an image. Always include it. | `<img src="..." alt="Graph of y = x^2">` |
| 18 | `width` / `height` | `<img>`, `<canvas>`, `<video>`, `<iframe>` | Size in pixels. | `<canvas width="600" height="400">` |
| 19 | `type` | `<input>`, `<button>`, `<script>` | The kind of input or button, or the kind of script. | `<input type="range">` |
| 20 | `name` | `<input>`, `<select>`, `<textarea>` | The name the value is sent under when a form is submitted. | `<input name="problem">` |
| 21 | `value` | `<input>`, `<option>`, `<button>` | The starting value, or the value sent for that choice. | `<input type="number" value="5">` |
| 22 | `placeholder` | `<input>`, `<textarea>` | Grey hint text shown while the box is empty. | `<input placeholder="2x + 3 = 7">` |
| 23 | `for` | `<label>`, `<output>` | Connects to the input with the matching `id`. | `<label for="problem">` |
| 24 | `min` / `max` / `step` | `<input>` (number, range, date) | Lowest value, highest value, and how much each step moves. | `<input type="range" min="-5" max="5" step="0.5">` |
| 25 | `required` | `<input>`, `<select>`, `<textarea>` | The form cannot be submitted while this is empty. | `<input required>` |
| 26 | `checked` | `<input>` (checkbox, radio) | Ticked by default. | `<input type="checkbox" checked>` |
| 27 | `selected` | `<option>` | The default choice in a drop-down. | `<option selected>` |
| 28 | `disabled` | `<button>`, `<input>`, `<select>` | Greyed out and cannot be used. | `<button disabled>` |
| 29 | `rows` / `cols` | `<textarea>` | Height in lines and width in characters. | `<textarea rows="4" cols="40">` |
| 30 | `action` / `method` | `<form>` | Where the form data is sent, and how (`get` or `post`). | `<form action="/send" method="post">` |
| 31 | `controls` | `<video>`, `<audio>` | Shows play, pause and volume buttons. | `<video src="..." controls>` |
| 32 | `defer` | `<script>` | Runs the script after the page has loaded. | `<script src="app.js" defer>` |
| 33 | `colspan` / `rowspan` | `<td>`, `<th>` | Make a cell stretch across several columns or rows. | `<td colspan="2">` |
| 34 | `open` | `<details>` | Starts the section opened. | `<details open>` |

## 3. ELEMENTS

An element is the whole unit: opening tag + content + closing tag. Example:

```html
<a href="https://developer.mozilla.org" target="_blank">MDN</a>
<!-- <a ...>  = opening tag, with 2 attributes: href and target -->
<!-- MDN      = content (what users see) -->
<!-- </a>     = closing tag -->
```

### Void (self-closing) elements

These have no content and **no closing tag**: `<meta>`, `<link>`, `<img>`, `<input>`, `<br>`, `<hr>`. (You may see them written as `<br />`; the `/` is optional in HTML5.)

### Block vs inline

| Type | Behaviour | Tags from this note |
| --- | --- | --- |
| Block | Starts on a new line and takes the full width | `<h1>`-`<h6>`, `<p>`, `<div>`, `<ul>`, `<ol>`, `<li>`, `<table>`, `<form>`, `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<pre>`, `<blockquote>`, `<hr>`, `<details>` |
| Inline | Stays inside a line of text | `<a>`, `<span>`, `<strong>`, `<em>`, `<code>`, `<sub>`, `<sup>`, `<br>`, `<img>`, `<input>`, `<button>`, `<select>`, `<textarea>`, `<label>`, `<output>`, `<canvas>` |

### Nesting rules

- Close tags in the reverse order you opened them: `<p><strong>Hi</strong></p>`, not `<p><strong>Hi</p></strong>`.
- Do not put block elements inside inline ones (no `<div>` inside a `<span>`), and never put a `<p>` inside another `<p>`.
- `<li>` only goes directly inside `<ul>` or `<ol>`; `<tr>` inside `<table>`; `<td>`/`<th>` inside `<tr>`; `<option>` inside `<select>`.
- Indent nested tags (2 spaces or 1 tab) so you can see the structure. In VS Code, Shift + Option + F formats the file for you.

## Related
- [[HTML Basics]]
- [[Use of Tags]]
- [[Lines Used HTML]]
- [[CSS Selectors]]
