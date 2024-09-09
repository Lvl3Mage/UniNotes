HTML is a language based on tags. The HTML defines the basic structure (scaffolding) of a website.

## HTML tags
These are the building blocks of HTML. This is what a typical HTML tag looks like:
![[HTMLTagExample1.svg]]
>[!warning] Self closing tags
>Some tags open close in one tag. These tags cannot have any content. 
>Example:
>
>![[HTMLTagSelfClosing.png]]
<div style="page-break-after: always;"></div>

### Important tags

#### `<body>`

**Use Case:** Contains the content of the HTML document, such as text, images, links, and other media.

**Code Snippet:**
```html
<body>
    <h1>Welcome to My Web Page</h1>
    <p>This is a paragraph of text.</p>
</body>
```

#### `<h1> to <h6>`

**Use Case:** Defines HTML headings, with `<h1>` being the highest (or most important) level and `<h6>` the lowest.

**Code Snippet:**
```html
<h1>Main Heading</h1>
<h2>Subheading</h2>
<h3>Sub-subheading</h3>
```

#### `<p>`

**Use Case:** Represents a paragraph of text.

**Code Snippet:**
```html
<p>This is a paragraph of text that provides information.</p>
```

#### `<a>`

**Use Case:** Defines a link, used to link from one page to another.

**Code Snippet:**
```html
<a href="https://www.example.com">Visit Example</a>
```

<div style="page-break-after: always;"></div>


#### `<img>`

**Use Case:** Embeds an image into the HTML document.

**Code Snippet:**
```html
<img src="./path/to/image.jpg" alt="Description of the image">
```

#### `<ul>` and `<li>`

**Use Case:** Creates an unordered (bulleted) list.

**Code Snippet:**
```html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

#### `<ol>` and `<li>`

**Use Case:** Creates an ordered (numbered) list.

**Code Snippet:**
```html
<ol>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>
```

#### `<div>`

**Use Case:** A block-level container for grouping content. Has `display: block` by default.

**Code Snippet:**
```html
<div>
    <h2>Section Title</h2>
    <p>This is a section of content within a div.</p>
</div>
```

<div style="page-break-after: always;"></div>


#### `<span>`

**Use Case:** An inline container for grouping text or elements. Has `display: inline` by default. Useful when you want the text to continue flowing normally all the while grouping some of it under a common element

**Code Snippet:**
```html
<p>This is a <span style="color: red;">red</span> word in a sentence.</p>
```

#### `<input>`

**Use Case:** Defines an input field within a form. 
- The **type** attribute specifies the type of the field: *text, number, date, range* are common examples
- The **value** attribute specifies the value within the input.

**Code Snippet:**
```html
<input type="text" id="name" name="name">
<input type="submit" value="Submit">
```

####  `<button>`

**Use Case:** Represents a clickable button.

**Code Snippet:**
```html
<button type="button">Click Me!</button>
```

<div style="page-break-after: always;"></div>


####  `<table>`, `<tr>`, `<th>`, and `<td>`

**Use Case:** Defines a table, table row (tr), table header (th), and table data (td).

**Code Snippet:**
```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>
```

####  `<link>`

**Use Case:** Used to link external resources such as stylesheets, web fonts, or icons to the HTML document.

**Code Snippet:**
```html
<head>
    <link rel="stylesheet" href="styles.css">
    <link rel="icon" href="favicon.ico" type="image/x-icon">
</head>
```

- `rel="stylesheet"`: Specifies the relationship between the current document and the linked file.
- `href="styles.css"`: The URL of the linked resource.
- `type="image/x-icon"`: Specifies the MIME type of the linked resource.

<div style="page-break-after: always;"></div>


####  `<script>`

**Use Case:** Used to embed or reference executable code, typically JavaScript.

**Code Snippet:**
```html
<body>
    <h1>My Web Page</h1>
    <p>This is a paragraph of text.</p>
    <script>
        // Inline JavaScript code
        console.log('Hello, World!');
    </script>
    <script src="script.js"></script>
</body>
```

- `<script src="script.js"></script>`: References an external JavaScript file.
- `<script> ... </script>`: Contains inline JavaScript code that will be executed when the HTML document is loaded.
>[!warning] Place your script tags after your main HTML
>It's usually a good idea to place all the script tags right before the closing body tag, after all of your HTML. This is because if your JS interacts with your HTML and is placed above it **there won't be any html to interact with** when the script executes.

<div style="page-break-after: always;"></div>

### Attribute structure
Tag attributes are used to include additional information on a tag.

![[HTMLTagExample2.svg]]
>[!warning] 
>Attribute values are **always** **strings** when you access them through js
<div style="page-break-after: always;"></div>

### Important attributes

### `href`

**Use Case:** Specifies the URL of the page the link goes to.

**Code Snippet:**
```html
<a href="https://www.example.com">Visit Example</a>
```

### `src`

**Use Case:** Specifies the URL of the image, script, or iframe.

**Code Snippet:**
```html
<img src="image.jpg" alt="Description of the image">
<script src="script.js"></script>
```

### `value`

**Use Case:** Specifies the initial value of an input element.

**Code Snippet:**
```html
<input type="text" value="Default text">
<input type="submit" value="Submit">
```

### `style`

**Use Case:** Specifies inline CSS styles for an element.

**Code Snippet:**
```html
<p style="color: blue; font-size: 20px;">This is a styled paragraph.</p>
```

<div style="page-break-after: always;"></div>


### `class`

**Use Case:** Specifies one or more class names for an element, used for CSS and JavaScript targeting.

**Code Snippet:**
```html
<p class="highlight">This paragraph is highlighted.</p>
<p class="highlight highlight-different">This is another highlighted paragraph.</p>
```

### `id`

**Use Case:** Provides a unique identifier for an HTML element. Can be used to style elements via CSS or select them with JS

**Code Snippet:**
```html
<p id="intro">This is an introductory paragraph.</p>
<a href="#intro">Go to Intro</a>
```

### `onClick`

**Use Case:** Executes JavaScript code when an element is clicked.

**Code Snippet:**
```html
<button onClick="alert('Button clicked!')">Click Me!</button>
```

### `type`

**Use Case:** Specifies the type of an input element.

**Code Snippet:**
```html
<input type="text" name="username">
<input type="password" name="password">
<input type="submit" value="Login">
<input type="radio" name="payment" value="paypal"> Paypal
<input type="radio" name="payment" value="cash"> Cash
<input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter
```



<div style="page-break-after: always;"></div>

## Basic page structure
The basic structure looks like this:
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>(Name on the browser tab)</title>
	(links to include css)
</head>
<body>
	(website content)
	(script tags for js)
</body>
</html>

```