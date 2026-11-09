Detailed notes for every tag in [[HTML Tags, Elements, Attributes]]. Numbers match the table.

## Page structure

1. `<!DOCTYPE>`:
	1. The `html` part isn’t an attribute. It’s just the name of the document type, and in HTML5 it’s always exactly `<!DOCTYPE html>`. 
	2. It isn’t case-sensitive: `<!doctype html>` works too.
	3. It is a declaration, not a real tag, so it has no attributes and no closing tag.
	4. Without it, browsers switch to "quirks mode" and copy old 1990s bugs, so CSS may look wrong.
2. `<html>`:
	1. The root element: every other tag goes inside it. Only one per page.
	2. Holds exactly two things: `<head>` then `<body>`.
	3. Always add `lang` (e.g. `lang="en"`): it helps screen readers, translation and search engines.
	4. Other attributes you might see: `dir="rtl"` for right-to-left languages, `class` or `data-theme` for dark mode.
3. `<head>`:
	1. Goes right after `<html>`, before `<body>`. Only one per page.
	2. Holds `<meta>`, `<title>`, `<link>`, `<style>` and sometimes `<script>`.
	3. Nothing inside it is shown on the page itself; it is instructions for the browser and search engines.
4. `<meta>`:
	1. A void element: no closing tag.
	2. `<meta charset="UTF-8">` should be the first thing in `<head>` so letters and symbols display correctly.
	3. `<meta name="viewport" content="width=device-width, initial-scale=1.0">` makes the page fit phone and Chromebook screens. Always include it.
	4. `name="description"` gives the short summary search engines show under your page title.
5. `<title>`:
	1. Goes inside `<head>`. Only one per page.
	2. Keep it short and specific, e.g. "MCR3U Functions | SeeSolve".
6. `<link>`:
	1. A void element: no closing tag. Goes in `<head>`.
	2. `rel` says what kind of file it is: `stylesheet` for CSS, `icon` for the tab icon, `manifest` for a PWA manifest.
	3. `href` is the path to the file.
	4. Not the same as `<a>`: `<link>` is invisible and loads a file; `<a>` is a clickable link.
7. `<style>`:
	1. Usually in `<head>`.
	2. Fine for small tests, but for real projects put CSS in a separate file and use `<link>`, so many pages can share it.
8. `<script>`:
	1. Always needs a closing `</script>`, even when using `src`.
	2. Put it at the end of `<body>`, or add `defer`, so the HTML loads before the code runs.
	3. `type="module"` turns on `import` and `export` (SeeSolve uses this).
9. `<body>`:
	1. Comes after `</head>`. Only one per page.
	2. All visible content (text, images, forms, tables) goes here.

## Page layout

10. `<header>`:
	1. Not the same as `<head>` (invisible info) or `<h1>` (a heading). `<header>` is a visible area.
	2. A page can have more than one, e.g. one for the page and one at the top of an `<article>`.
11. `<nav>`:
	1. Usually contains a `<ul>` of links.
	2. Screen readers let users jump straight to it, so use it for the main menu.
12. `<main>`:
	1. Only one visible `<main>` per page.
	2. Do not put headers, menus or footers that repeat on every page inside it.
	3. In SeeSolve, `<main id="app">` is where each screen is drawn.
13. `<section>`:
	1. Give each section a heading (`<h2>` etc.).
	2. Use `id` so links like `<a href="#courses">` can jump to it.
14. `<article>`:
	1. Test: could you post it somewhere else by itself and it still makes sense? Then it is an `<article>`.
15. `<aside>`:
	1. Often shown as a sidebar with CSS.
16. `<footer>`:
	1. `&copy;` shows the copyright symbol.
	2. A good place to credit the libraries you use.
17. `<div>`:
	1. Block-level: starts on a new line.
	2. Use it when none of the meaningful tags (`<section>`, `<nav>`, `<article>`...) fit.
	3. Almost always used with `class` or `id`.
18. `<span>`:
	1. Inline: stays in the same line of text.
	2. The inline version of `<div>`.

## Text

19. `<h1>` to `<h6>`:
	1. Use one `<h1>` per page for the main title.
	2. Do not skip levels (`<h1>` then `<h3>`). Screen readers use headings like a table of contents.
	3. Choose by importance, not size; change the size with CSS.
20. `<p>`:
	1. Block-level: each paragraph starts on a new line with space around it.
	2. Extra spaces and line breaks you type inside are ignored by the browser.
21. `<br>`:
	1. A void element: no closing tag.
	2. Use it for line breaks that are part of the content (addresses, poems), not to add space between things; use CSS for spacing.
22. `<hr>`:
	1. A void element: no closing tag.
23. `<strong>`:
	1. Screen readers can stress it.
	2. `<b>` also makes bold text but without the "important" meaning; prefer `<strong>`.
24. `<em>`:
	1. `<i>` also makes italics but without the emphasis meaning; prefer `<em>`.
25. `<sub>` / `<sup>`:
	1. Perfect for SeeSolve: chemical formulas (H2O) and exponents (x squared).
26. `<code>`:
	1. Inline, for code inside a sentence.
	2. Wrap it in `<pre>` for blocks of code.
27. `<pre>`:
	1. Normally HTML ignores extra spaces; `<pre>` does not.
	2. Used with `<code>` to show multi-line code or ASCII diagrams.
28. `<blockquote>`:
	1. `cite` can hold the web address the quote came from.
29. `<!-- -->`:
	1. Not shown on the page, but anyone can see it with View Source, so never put passwords in comments.
	2. In VS Code, select lines and press Cmd + / to comment them out.

## Links and media

30. `<a>`:
	1. `href` is the destination. A full web address goes to another site; `page.html` goes to your own file; `#courses` jumps to the element with `id="courses"`.
	2. `target="_blank"` opens the link in a new tab.
	3. The text between the tags is what users click, so make it descriptive ("Course list", not "click here").
31. `<img>`:
	1. A void element: no closing tag.
	2. `alt` describes the image for screen readers and shows if the image fails to load. Always include it.
	3. Setting `width` and `height` stops the page from jumping around while the image loads.
32. `<video>`:
	1. `controls` shows the play button and volume. Without it, users cannot play the video.
	2. `<audio>` works the same way for sound files.
33. `<iframe>`:
	1. YouTube gives you the code: Share, then Embed.
	2. Add a `title` so screen readers know what it is.
34. `<canvas>`:
	1. Empty until JavaScript draws on it.
	2. SeeSolve uses it for the physics sandbox and atom diagrams; Three.js also draws 3D onto a canvas.

## Lists

35. `<ul>`:
	1. Only `<li>` elements go directly inside it.
	2. Menus are usually a `<ul>` of links styled with CSS.
36. `<ol>`:
	1. Use it when order matters, like steps.
	2. `start="5"` starts counting at 5; `type="a"` uses letters.
37. `<li>`:
	1. Can contain other tags, even another list (a nested list).

## Tables

38. `<table>`:
	1. Use tables for data only (like the interest table), not for page layout; use CSS for layout.
	2. Optional `<thead>` and `<tbody>` group the header and body rows.
39. `<tr>`:
	1. Each row holds `<th>` or `<td>` cells.
40. `<th>`:
	1. Helps screen readers understand the table.
	2. `colspan="2"` makes a cell stretch across 2 columns.
41. `<td>`:
	1. `rowspan="2"` makes a cell stretch down 2 rows.

## Forms and inputs

42. `<form>`:
	1. Pressing Enter in an input or clicking a submit button submits the form.
	2. `action` is where data is sent and `method` is how (GET or POST). SeeSolve handles the form with JavaScript instead, so it does not need them.
43. `<label>`:
	1. `for` must match the input's `id`. Then clicking the label focuses the input, and screen readers read the label.
	2. Or wrap the input inside the label, as in the Learn Mode checkbox.
44. `<input>`:
	1. A void element: no closing tag.
	2. Common types: `text`, `number`, `range` (slider), `checkbox`, `radio`, `email`, `password`, `color`, `date`, `file`, `submit`.
	3. `placeholder` is grey hint text; `value` is the starting value.
	4. `min`, `max` and `step` limit `number` and `range` inputs (used for SeeSolve sliders).
	5. `required` stops the form from submitting while empty; `checked` ticks a checkbox by default.
45. `<button>`:
	1. Inside a form, a button submits it unless you write `type="button"`.
	2. `disabled` greys it out so it cannot be clicked.
46. `<select>`:
	1. Holds `<option>` elements.
	2. Add `multiple` to let users choose more than one.
47. `<option>`:
	1. `value` is what the code receives; the text between the tags is what users see.
	2. `selected` makes it the default choice.
48. `<textarea>`:
	1. Needs a closing tag, unlike `<input>`.
	2. Used in SeeSolve's Code Lab for typing Python.
49. `<output>`:
	1. JavaScript updates its text when inputs change.

## Interactive

50. `<details>` / `<summary>`:
	1. `<summary>` is the clickable title; everything else inside is hidden until opened.
	2. `open` makes it start opened. Great for hints in Learn Mode.

