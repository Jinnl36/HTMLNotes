# HTML Basics
#html

## 1.1 What is HTML

HTML is HyperText Markup Language, it is the **structure** of a website or a page and what is on it. CSS makes it look good, JavaScript makes it do things. 

## 1.2 Specifying Character Encoding Standart
```html
<meta charset = "UTF-8">
```
UTF-8 is the default encoding standard used by HTML 5, and is recommended for use in 
***all*** modern web applications. For more, visit [UTF-8 Wiki](https://en.wikipedia.org/wiki/UTF-8)

## 1.3 HTML Syntax: Elements, Tags, and Comments

### 1.3.1 DOCTYPE declaration

```html
<!DOCTYPE html>
```
This is the most standard way to declare that this file is going to be written in HTML 5.  Each file must have one at the first row to inform the browser of the HTML version.

### 1.3.2 Elements 

```html
<p> content </p>
```
This phrase is a ***Element***, it is a entire unit made up of a opening tag, content, and closing tag

### 1.3.3 Tags

```html
<p>
```
This is a ***opening tag***, it indicates the start, and indicates to the browser the type of content they enclose, instructing the browser on how to process it.

```html
</p>
```
This is a ***ending tag***, it indicates the end of a element.

### 1.3.4 Block-Level and Inline Elements

 - In html, there are 2 types of elements:
	 - block-level elements
		 - These elements are used to create the main structure of a web page, including headers, paragraphs, and lists. Any content placed inside a block-level element will create a new block of content.
	 - inline elements
		 - Style content within block-level elemetns such as links and images.
  	
```html
	<!--Block Level Elements-->
	<!--Headers 1 through 6, Each repersenting a different size-->
	<h1>
	<!--P for paragraphs-->
	<p>
	<!--For lists-->
	<ul>
	<!--For lists-->
	<ol>
	<!--For grouping content, ie divider-->
	<div>
```

 ```html
 <!--Inline Elements-->
 <!--For Links-->
 <a>
 <!--For Images-->
 <img>
 <!--For Styling Content-->
 <span>
 
 ```
### 1.3.4 HTML Comments
```html
<!-- Comment -->
```
This is a example of content, starting with <!--, ending with -->

## 1.4 Attributes and Values

Attributes provide additional information about an element, ie style, source, or behavior.

You can add attributes to an HTML element by using the attribute name, followed by an equal sign and the attribute value. This value can be enclosed in quotes, single quotes, or left unquoted.

```html
<img src = "image.jpg" alt = "A detached house"
```

In this example, src is the attribute and the "image.jpg" is the value. For the img function, the most used attributes are the src and alt, repersenting the source of picture and the text description respectively.

## 1.5 Global vs. Element Specific attributes

 - Global attributes can be applied to any HTML element. They have a wide range of purposes, such as assigning unique identifiers, adding classes for styling, or providing additional information on an element.
	 - Examples include id, class, style, and title.

 - Element specific attributes are specific to particular HTML elements and cannot be used with ***all*** elements. They provide special functionality or modify the behavior of specific elements, making them essential for proper usage of those elements.
	 - Examples include href (specific to a elements), src (specific to img and media elements), and type (specific to input elements).

 - Understanding and acknowledging the difference between global and element specific attributes is crucial for using HTML.
## 1.6 HTML, Head, and Body

### 1.6.1 The HTML Tag

 - The HTML tag is one of the ***most important tags*** in an HEML document, it defines the entire web page and serves as the starting point for every document. It is always the first tag after the DOCTYPE in every HTML document.
 - Everything in the document appears between these two tags, it does ***any attributes*** associated with it. An example would be:

 ```html
<!DOCTYPE html>
<html>
   <!-- The hidden content of an HTML document: the head section will    go here. -->
   <!-- The visible content of an HTML document: the body section        will go here. -->
</html>
 ```

### 1.6.2 The Head Section

 - The *head* section is an important component of an HTML document, it contains the information used by the browser to display and interact with the web page. It can optimize the web page and furnish additional context.
	 1. ***PageTitle***, ie. the title of the web page that appears in the title bar of the browser and is used by search engines to display the page title in search results
	 2. ***Metadata***, includes the description and keywords that are used by search engines to index and rank the web page, instructions for web crawlers how to index and display the web page.
	 3. ***Links to external files***, this includes CSS stylesheets and Java Script files that add styling and functionality to the web page
	 4. ***Character Encoding***, which tells the browser that character set to use when displaying the web page.
```html
<!DOCTYPE html>
<html>
	<head>
		<!--1-->
		<title>My Web Page</title>
		<!--2-->
		<meta name="author" content="Peter Jackson">
		<!--3-->
		<link rel="stylesheet" href="styles.css"> <script                     src="script.js"></script>
		<!--4-->
		<meta charset="UTF-8">
	</head>
</html>
```
### 1.6.3 The Body Section

 - The *body* section contains the actual content that is displayed to the user. The two sections work together; the head provides instructions to the browser on how to display the content in the body section.
 - Examples of the content that you ca include in the body section are:
	 1. ***Text:*** headings, paragraphs, and other text elements to present your content to the user.
	 2. ***Images:*** you can include all types of images, such as photos, icons, and logos to make you page more beautiful.
	 3. ***Videos:*** You can add video content.
	 4. ***Forms:*** You can create elements that allow users to interact and submit information.
	 5. ***Links:*** You can include links to other pages.
	 6. ***Lists:*** You can use lists to organize content, including unordered and ordered lists.
	 7. ***Tables:*** You can use tables to present data in a structured way, such as pricing information.
### 1.7 Understanding the Interaction Between HTML, CSS, and JavaScript
 - HTML, CSS, and JavaScript are the three primary technologies used in web dev to create dynamic, engaging web pages.
	 - HTML provides the basic structure and content
	 - CSS defines the presentation of the HTML content ie layout, colours, and fonts
	 - Java Script adds interactivity to the web page
### 1.8 The Document Object Model (DOM)

 - DOM is a powerful tool that allows web devs to change the content and structure of an HTML doc using JavaScript
 - When a web page is loaded, DOM is created as a memory repersentation of the pages' content and structure. Devs can then use js to manipulate the DOM, dynamically adding, removing and changing the web page.
 - The DOM repersents the HTML document like a tree structure, consisting of nodes.

![[截屏2026-10-15 下午5.50.01.png]]
![[截屏2026-10-15 下午5.50.21.png]]

 - The DOM tree repersents the structure of a HTML document with 3 levels:
	 1. Document
	 2. HTML
	 3. Head/Body
 - Overall, DOM enables access and modifying the content and structure of HTML documents using JavaScript.
# 2 Formatting

## 2.1 Paragraphs and Text Formatting

 - In HTML, paragraphs are defined using the  `<p>` tag.
 - This indicates that the enclosed text should be treated as a seperate paragraph
	 1. `<strong>` tag is used to make enclosed text bold
	 2. `<em>` is used to make text italic
	 3. `<u>` is used to underline
	 4. `<sup>` is used to superscript enclosed text
	 5. `<sub>` is used to subscript enclosed text
	 6. `<del>` is used to strike through text
	 7. `<mark>` is used to highlight text
	 8. `<q>` is used for short inline quotes
	 9. `<blockquote>` is used for longer, blocked quotes, seperated from paragraphs
	 10. `<cite>` is used to markup the title of a source; can also be used in `<q>` for making the enlosed text cited with a link
	 11. `<footer>` creates a footer
	 12. `<br>`creates a new line of text within `<p>` tags
	 13. `<hr>` creates a horizontal line breaking paragraphs up
	 14. `<code>` displays inline code snippets
	 15. `<pre>`displays text like code, preserving all characters and displays the txt in a monospaced font
	 16. `<kbd>` displays keyboard input; displayed in a monospace font, in a rectangular box, indicates that it represents keyboard input
	 17. `<samp>` indicates sample output; in monospace font, emphasized in some special way, such as bold or italic
	 18. Lists:
		 1. `<ul>` Unordered list, displays a list with no particular order
		 2. `<ol>` Ordered list, list of items in a specific order
		 3. `<dl>` list of terms with their definitions
			 1. `<dt>` to indicate the list items
			 2. `<dd>` to indicate the definition of the items
	 19. ***You can nest a list in a list, sub-indented use `<li>` to state the items in the list***
	 20. Tables:
		 1. `<table>` defines the entire table. Attributes:
			 1. border, sets the border size of table
			 2. cellspacing, sets the space between cells in table
			 3. cellpadding, sets the space between the cell contend and the cell border
			 4. width, which sets the width of the table
			 5. height, sets the height of the table
			 6. align, sets tahe horizontal alignment of the table
			 7. bgcolor, sets the background color of the table
	 21. `<tr>` defines a row within the table
	 22. `<td>` defines a cell within a row
	 23. `<th>` works the same as a `<td>` but is used to define header cells
	 24. colspan and rowspan attributes specify how many columns a cell should span. Rowspan attribute specifies how many rows a cell should span.
	 25. `<caption>` used to add a title or caption to an HTML table, placed immediately after the
	 26. `<summary>` It gives a summary of table for users who use screenreaders
## 3 Visual and Interactive Elements

### 2.1 Images

 - `<img>` has important attributes:
	1. `<src>` specifies the source URL of the image that should be displayed
	2. `<alt>` provides alternative text that will be displayed if the image cannot be loaded, also used by screen readers
	3. `<width>` specifies the width of the image
	4. `<height>` works with width to specifies the height of the image
- Image formats include JPEG, PNG and GIF:
	1. JPEG -  Joint Photographic Experts Group, Best suited for photographs or images with many colors and gradients. They are compressed which means they have a smaller file size, but results in a loss of quality
	2. PNG - Portable Network Graphics, Best suited for images with transparent backgrounds or images with sharp edges. PNG images are lossless which means they do not lose quality when compressed
	3. GIF - Graphics Interchange Format, Best suited for simple animated graphics with limits colours.
	4. SVG - Scalable Vector Graphics, images that need to be scaled without losing quality
	5. WebP, offers better compression and smaller file sizes
- Paths for `<src>`:
	- A relative path is a path that **starts from the directory of the HTML file**.
	- An absolute path is a path that starts from the root directory of the website 
- Responsive Images:
	- `<srcset>` allows you to specify a list of image files with different resolutions, sizes, and formats. When browser loads the image, it will select the most appropriate image from the list based on the screen size and the capability of the device
	- `<sizes>` specifies the size of the image container in which the image will be displayed. It tells the browser how much screen space the image will occupy on different devices
![[截屏2026-10-23 下午1.15.51.png]]
![[截屏2026-10-23 下午1.15.51.png]]
 - In this code, it sets the source of the image to sunflowers.jpg
 - the alt attribute provides the following alternative text for the image
 - the srcset provides 3 different versions of the image with different sizes and resolutions
 - The sizes attribute defines the width of the image at different breakpoints
### Hyper Links
 - `<a>` In HTML, you can easily create links using this tag, which stands for "anchor".
	 - This tag relies on the `<herf>` attribute, which specifies the destination of the link
	 - The destination can be an absolute URL or a relitive URL (if the target page resides in the same directory as the current page)
	 - By quoting some text in the `<a></a>`tags, we can hyperlink the text inside and if clicked would bring to the links.
	 - You can also create links that point to specific sections within a web page. Such links are called anchor links or jump links
	 - The target="_blank" attribute will **open the linked page in a new tab or window**, allowing users to easily return to your website. The target="_self" attribute will open the link in the same window.
```html 
	   <!--EXAMPLE-->
	   <a href="https://www.example.com/" target="_blank">Visit our website</a>
```
 -  Email and Telephone Links:
 - To create an email link, you can use the mailto protocal fallowed by the email address that you want to link to.
 - The target="_blank" attribute will **open the linked page in a new tab or window**, allowing users to easily return to your website. The target="_self" attribute will open the link in the same window.
 - Similarly, to create a telephone link, you can use the `tel` protocol followed by the telephone number that you want to link to. 
 - The download attribute specifies that the target of the link should be downloaded rather than navigated to. The attribute value can be used as the default filename that the downloaded file will be saved as.
 - The rel attribute specifies the relationship between the current document and the target document. It can be used to indicate that the target document is a stylesheet, a parent document, or a part of a series, among other things.
 - The title attribute provides additional information about an element, enhancing the user's understanding and interaction with web content.
 - To make an element clickable, you simply need to wrap the `<a>` tag around it. The href attribute within this tag defines the URL to which the link points.
### Forms
 - To create a form, you must use the `<form>` element. Inside the `<form>` element, you can add various input fields, such as text input, radio buttons (Single Choice), checkboxes, and more.
 - The `<form>` element typically includes:
	 - The `action` attribute, which specifies the URL of the server-side script or endpoint that will process the form data. The action attribute is added to the `<form>` attribute. When the from is submitted the browser will send the form data to the specific URL.
	 - The `method` attribute, which specifies the HTTP method (GET or POST) used when sending form data to the server. The `method` attribute is added to the `<form>` element and its value is set to either `"GET` or `"POST"`
### The GET and POST Methods
 - To allow users to submit form data, you must choose the way the data gets sent. This is called the HTTP Method.
 - The HTTP methos, also known as the HTTP request method, is a verb that indicated the desired action to be performed on a resource identified by a url.
 - The GET method **sends the form data in the URL query string**. This means that the form data is visible in the browser's address bar and can be bookmarked or shared with others.
 - The POST method **sends the form data in the body of the HTTP request**. This means that the form data is not visible in the URL or the browser's address bar. It's commonly used for more complex forms that require higher security, such as login forms or forms that contain sensitive information. However, the form data cannot be bookmarked, shared, or cached by the browser as in the case of the GET method.
### The `<input>` Element
 - The `<input> `element is used to **create different types of input fields** used to collect user data. It can be configured to accept various types of data, such as text, passwords, numbers, and emails, among others, through the use of the type attribute.
 - Common input types (the type attribute values) include:
	 - text - a single-line text input feild, used for short text inputs such as names, email addresses, etc.
	 - email - a single-line text input field used specifically for entering and validating email adresses
	 - url - a single-line input feild used specifically to validate and accept only numbers
	 - password - a single-line text input field that masks the entered characters to maintain the confidentiality of the password
	 - checkbox - a checkbox that can be toggled on or off, allows users to select one or more options from a list
	 - radio - a radio button that belongs to a group of radio buttons
	 - submit - a button that submits the form data and sends it to the server as specified by the action and method attributes
	 - reset - a button that clears the form data and resets it to the enitial values
	 - This can be used like `type = "text"`
	 - Each input field must have a name attribute
	 - Adding the required attribute to an input field makes it mandatory for users to fill out that field before submitting the form. It's a simple way to ensure that critical information is not omitted.
### The `<label>` Element
 - The `<label>` element plays a vital role in creating accessible and user friendly forms. It provides a textual description for each input field, improving from readability and usability.
 - By **associating a label with a specific input field** using the for attribute (which should match the input's id attribute), users can click on the label to focus on the corresponding input, a feature particularly beneficial for those using assistive technologies.
 - `<label for="email">Email:</label>` creates a label for the input field. The for attribute of the label is set to "email," which means this label is associated with an input element whose id attribute is "email." The text "Email:" is displayed to the user next to the input field, indicating what information is expected in the associated input field.
 - `<input type="email" id="email" name="useremail" required> `defines an input field designed to receive an email address:
	 - `type = "email"` specifies that the input should be an email address. Modern browsers will check if the entered text is in the format of an email address and prompt the user if it is not.
	 - `id="email"` assigns an identifier to the input field, linking it with the label through the for attribute. This enhances accessibility, as clicking on the label will focus the input field.
	 - `name="useremail"` names the data entered into this field as "useremail," which is used to identify the form data on the server side once submitted.
	 - `required` marks the field as mandatory, meaning the form cannot be submitted without an email address entered in this field.
### Enhancing Forms With Key Elements: `<text area>`, `<select>`, `<button>`, and `<fieldset>`
 - In addition to the `input` element, there are other form elements that you can use in HTML forms. Some of them include `<textarea>`, `<select>`, `<button>`, and `<fieldset>`.
 - The `<textarea>` element creates a multi-line text input field, which allows users to enter larger amounts of text. You can set the `rows` and `cols` attributes to control the visible size of the textarea.
 - The `<select>` element creates a dropdown list, used with `<option>` elements to define the available options. You can use the multiple attribute to allow multiple selections, and the size attribute to control the number of visible options.
 - The `<button>` button element creates a clickable button that can be customized with JavaScript or used to submit or reset a form, depending on its type attribute (e.g., submit, reset, or button). If the type attribute is omitted or set to "button", it does not have any default behavior and can be controlled with JavaScript.
 - The `onclick` attribute is a JavaScript event handler that specifies the action to be performed when the button is clicked. In this case, the action is an `alert()` function call, which displays the pop-up dialog message we've mentioned above
 - The `<fieldset>` element creates a container used to group together related form elements. It can be helpful in organizing complex forms with multiple sections. The `<legend>` element can be used within a `<fieldset>` to provide a caption or title for the group.
### Mastering Form Attributes: _value_, _placeholder_, _disabled_, and _readonly_
 - The value attribute specifies the initial value of the input field. When the form is loaded, this value will be **pre-filled in the input field**.
 - The placeholder attribute specifies **a hint that describes the expected value** of the input field. It does not specify the initial value itself, as in the case of the value attribute. The placeholder text is displayed in the input field when it is empty and **disappears when the user starts typing**.
 - The disabled attribute **disables the input field, making it uneditable and unselectable**. Users cannot interact with disabled fields, and the fields appear grayed out or visually distinct from other fields.
 - The readonly attribute **makes the input field read-only**, allowing users to view the content but not edit it. Unlike disabled fields, read-only fields are still **selectable and send their values** when the form is submitted. This attribute is useful when you want to display information to users that they should not edit but still include when submitting the form data.
The name attribute is essential for identifying each piece of data submitted. It acts as a key for the form data, allowing the server-side script to access and process user inputs based on these names.
### Diving Deeper into Form-Specific Attributes: _maxlength_, _min_, _max_, _autocomplete_, and _pattern_
 - maxlength limits the number of characters that can be entered into a text input field. 
 - min and max set the minimum and maximum values that can be entered into number, range, date, and time input fields. For example, the following line will limit the "age" input to a number between 18 and 100:
 - autocomplete – controls whether the browser should automatically complete input fields with previously entered data. This attribute can have values of "on" (default), "off", or "new-password" (to disable autocomplete for password fields). 
 - pattern specifies a regular expression that the input value must match in order to be valid. This attribute is useful for enforcing specific formatting or data validation rules. 
### Building an HTML Form
 - Start with the `<form>` element. This element wraps all the contents of your form, including input fields, labels, and buttons. The action attribute specifies where to send the form data when submitted, and the method attribute defines how to send it (usually POST or GET).
 - Input fields are where users enter data. Use the `<input>` tag to create these fields. The type attribute specifies the kind of data you expect (e.g., text, number, email). The name attribute is crucial for identifying the data on the server side.
 - The `<label>` element enhances the usability of your form by providing descriptive text for each input field. Link each label to its corresponding input by matching the for attribute in the `<label>` tag with the id attribute of the `<input>` tag.
 - Finally, add a submit button using `<input type="submit">` or `<button type="submit">`. This button sends the form data to the server.
 - 
```html
<!--Login Screen-->
<form action="/submit" method="POST">
  <label for="username">Username:</label>
  <input type="text" id="username" name="username" required>
  <br>
  
  <label for="password">Password:</label>
  <input type="password" id="password" name="password" required>
  <br>
  
  <input type="submit" value="Login">
  <input type="reset" value="Reset">
</form>
```

```html
<!--Contract Screen-->
<form action="/submit-contact" method="post">
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required>
  <br>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  <br>
  
  <label for="message">Message:</label>
  <textarea id="message" name="message" required></textarea>
  <br>
  
  <button type="submit">Send</button>
</form>
```

```html
<!--Simple BMI Calculator Form-->
<form action="/submit-bmi" method="post">
  <label for="weight">Weight (kg):</label>
  <input type="number" id="weight" name="weight" required>
  <br>
  
  <label for="height">Height (cm):</label>
  <input type="number" id="height" name="height" required>
  <br>
  
  <button type="submit">Calculate BMI</button>
</form>
```

```html
<!--This is a Expanded Form-->
<form action="/submit" method="POST">
  <label for="name">Full Name:</label>
  <input type="text" id="name" name="name" required>
  <br>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required>
  <br>
  
  <p>Choose your meal preference:</p>
  <label for="vegetarian">Vegetarian</label>
  <input type="radio" id="vegetarian" name="meal" value="vegetarian" required>
  <label for="non-vegetarian">Non-Vegetarian</label>
  <input type="radio" id="non-vegetarian" name="meal" value="non-vegetarian" required>
  <br>
  
  <p>Select the workshops you'd like to attend:</p>
  <label for="workshop1">Workshop 1</label>
  <input type="checkbox" id="workshop1" name="workshop1">
  <label for="workshop2">Workshop 2</label>
  <input type="checkbox" id="workshop2" name="workshop2">
  <label for="workshop3">Workshop 3</label>
  <input type="checkbox" id="workshop3" name="workshop3">
  <br>
  
  <input type="submit" value="Register">
</form>
```
