### Variable Declaration
```javascript
// Using var (function-scoped)
var x = 5;

// Using let (block-scoped, preferable for mutable variables)
let y = 10;

// Using const (block-scoped, constant value)
const PI = 3.14;
```

---
### Functions
#### Named Function
```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet('Alice')); // Output: Hello, Alice!
```
#### Anonymous Function
Anonymous functions are functions that can be created on the spot. You can store them in variables to later call them.
```javascript
let greet = function(name) {
    return `Hello, ${name}!`;
};

console.log(greet('Bob')); // Output: Hello, Bob!
```

---
<div style="page-break-after: always;"></div>


### Accessing the DOM (getting the HTML)

#### 1. **getElementById**

Retrieves an element by its ID attribute.

**Example:**
```javascript
let elementById = document.getElementById('myElementId');
console.log(elementById.textContent); // Output: Content of the element with ID 'myElementId'
```

#### 2. **getElementsByClassName**

Retrieves elements by their class name.

**Example:**
```javascript
let elementsByClass = document.getElementsByClassName('myClassName');
console.log(elementsByClass); // Output: List of elements with class 'myClassName'
```

#### 3. **querySelector**

Retrieves the first element that matches a specified CSS selector.

**Example:**
```javascript
let elementBySelector = document.querySelector('#myElementId .myClassName');
console.log(elementBySelector.textContent); // Output: Text content of the matched element
```

#### 4. **querySelectorAll**

Retrieves all elements that match a specified CSS selector.

**Example:**
```javascript
let elementsBySelectorAll = document.querySelectorAll('.myClassName');
console.log(elementsBySelectorAll) // Output: List of elements with class myClassName
```

<div style="page-break-after: always;"></div>


## Adding DOM Elements

JavaScript allows you to dynamically create and add elements to the DOM.

**Example:**

```javascript
// Create a new <div> element
let newDiv = document.createElement('div');

// Set attributes (optional)
newDiv.id = 'myNewDiv';
newDiv.className = 'new-div-class';

// Set inner text or HTML (optional)
newDiv.textContent = 'This is a new div element';

// Append the new element to an existing element
document.body.appendChild(newDiv);
```

## Changing Styles

You can modify the styles of DOM elements directly using JavaScript.

**Example:**

```javascript
// Get an existing element
let element = document.getElementById('myElementId');

// Change styles directly
element.style.backgroundColor = 'lightblue';
element.style.padding = '10px';
element.style.border = '1px solid black';
```

## innerHTML

`innerHTML` property allows you to get or set the HTML content inside an element.

**Example:**

```javascript
// Get HTML content
let htmlContent = document.getElementById('myElementId').innerHTML;

// Set HTML content
document.getElementById('myElementId').innerHTML = '<p style="opacity:0.5;">New HTML content</p>';
```


### Manipulating CSS Classes with `classList`

#### Description

The `classList` property of DOM elements in JavaScript provides methods to add, remove, toggle, and check for CSS classes on an element without directly manipulating the `className` property.

#### Usage

#### 1. **Adding a Class**

**Description:** Adds a CSS class to an element.

```javascript
let element = document.getElementById('myElementId');
element.classList.add('new-class');
```

#### 2. **Removing a Class**

**Description:** Removes a CSS class from an element.

```javascript
let element = document.getElementById('myElementId');
element.classList.remove('old-class');
```

#### 3. **Toggle a Class**

**Description:** Toggles the presence of a CSS class; adds the class if it's not present, removes it if it is.

```javascript
let element = document.getElementById('myElementId');
element.classList.toggle('active');
```

#### 4. **Check if a Class Exists**

**Description:** Checks if an element has a specific CSS class.

```javascript
let element = document.getElementById('myElementId');
if (element.classList.contains('highlight')) {
    // Do something
}
```
