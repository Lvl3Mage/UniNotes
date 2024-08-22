A CSS selector is a line of CSS code that applies CSS styles to HTML tags. Different CSS selectors will select different HTML tags. 
![[css-example.svg]]
<div style="page-break-after: always;"></div>


## CSS Selectors

### **Universal Selector (`*`)**

**Description:** Selects all elements on the page.

**Usage:**
```css
* {
    margin: 0;
    padding: 0;
}
```

**HTML:**
```html
<p>This paragraph will be selected.</p>
<div>This div will be selected.</div>
```

**What It Selects:**
- `<p>This paragraph will be selected.</p>`
- `<div>This div will be selected.</div>`

**What It Won't Select:**
- Nothing. The universal selector selects all elements.

<div style="page-break-after: always;"></div>

### **Element Selector**

**Description:** Selects all elements of a given type.

**Usage:**
```css
p {
    color: blue;
}
```

**HTML:**
```html
<p>This paragraph will be selected.</p>
<div>This div will not be selected.</div>
```

**What It Selects:**
- `<p>This paragraph will be selected.</p>`

**What It Won't Select:**
- `<div>This div will not be selected.</div>`

<div style="page-break-after: always;"></div>


### **Class Selector (`.`)**

**Description:** Selects all elements with a specific class attribute.

**Usage:**
```css
.highlight {
    background-color: yellow;
}
```

**HTML:**
```html
<p class="highlight">This paragraph will be selected.</p>
<p class="highlight hightlight-2">This paragraph will be selected.</p>
<p>This paragraph will not be selected.</p>
```

**What It Selects:**
- `<p class="highlight">This paragraph will be selected.</p>`
- `<p class="highlight hightlight-2">This paragraph will be selected.</p>`

**What It Won't Select:**
- `<p>This paragraph will not be selected.</p>`

<div style="page-break-after: always;"></div>


### **ID Selector (`#`)**

**Description:** Selects a single element with a specific ID attribute.

**Usage:**
```css
#intro {
    font-size: 20px;
}
```

**HTML:**
```html
<p id="intro">This paragraph will be selected.</p>
<p id="main">This paragraph will not be selected.</p>
```

**What It Selects:**
- `<p id="intro">This paragraph will be selected.</p>`

**What It Won't Select:**
- `<p id="main">This paragraph will not be selected.</p>`

<div style="page-break-after: always;"></div>


###  **Pseudo-class Selector: Hover (`:hover`)**

**Description:** Selects elements when the user hovers over them with the mouse. Needs to be combined with other CSS selectors to work. 

For example if you wanted to make all links turn red on hover you could do this:

**Usage:**
```css
a:hover {
    color: red;
}
```

**HTML:**
```html
<a href="#">Hover over this link to see the effect.</a>
<a href="#">This link will also change color on hover.</a>
<p>This paragraph will not change on hover.</p>
```

**What It Selects:**
- `<a href="#">Hover over this link to see the effect.</a>`
- `<a href="#">This link will also change color on hover.</a>`

**What It Won't Select:**
- `<p>This paragraph will not change on hover.</p>`
<div style="page-break-after: always;"></div>


## CSS styles

###  **color**

**Description:** Specifies the color of the text.

**Usage:**
```css
/* Named Colors */
.named-example {
    color: red;
}

/* Hex Colors */
.hex-example {
    color: #ff5733;
}

/* RGB Colors */
.rgb-example {
    color: rgb(255, 87, 51);
}

/* RGBA Colors */
.rgba-example {
    color: rgba(255, 87, 51, 0.5); /* 50% opacity */
}
```

**HTML:**
```html
<p class="named-example">This text is red.</p>
<p class="hex-example">This text is a hex color.</p>
<p class="rgb-example">This text is an RGB color.</p>
<p class="rgba-example">This text is an RGBA color with 50% opacity.</p>
```


<div style="page-break-after: always;"></div>

###  **background**

**Description:** Specifies the background of an element.

**Usage:**
```css
/* Background Color */
.color-example {
    background-color: lightblue;
}

/* Background Image */
.image-example {
    background-image: url('background.jpg');
    background-size: cover;
    background-repeat: no-repeat;
}

/* Gradient Background */
.gradient-example {
    background: linear-gradient(to right, red, yellow);
}
```

**HTML:**
```html
<div class="color-example">This div has a light blue background.</div>
<div class="image-example">This div has a background image.</div>
<div class="gradient-example">This div has a gradient background.</div>
```

<div style="page-break-after: always;"></div>


###  **font-size**

**Description:** Specifies the size of the font.

**Usage:**
```css
/* Pixels */
.pixels-example {
    font-size: 16px;
}

/* Ems */
.ems-example {
    font-size: 1.5em;
}

/* Rems */
.rems-example {
    font-size: 1.5rem;
}
```

**HTML:**
```html
<p class="pixels-example">This text is 16px.</p>
<p class="ems-example">This text is 1.5em.</p>
<p class="rems-example">This text is 1.5rem.</p>
```

<div style="page-break-after: always;"></div>


###  **font-weight**

**Description:** Specifies the weight (boldness) of the font.

**Usage:**
```css
/* Named Weights */
.normal-example {
    font-weight: normal;
}

.bold-example {
    font-weight: bold;
}

/* Numeric Weights */
.light-example {
    font-weight: 300;
}

.semibold-example {
    font-weight: 600;
}

.extrabold-example {
    font-weight: 800;
}
```

**HTML:**
```html
<p class="normal-example">This text is normal weight.</p>
<p class="bold-example">This text is bold.</p>
<p class="light-example">This text is light (300).</p>
<p class="semibold-example">This text is semibold (600).</p>
<p class="extrabold-example">This text is extrabold (800).</p>
```

<div style="page-break-after: always;"></div>


###  **margin**

**Description:** Specifies the space around elements.

**Usage:**
```css
/* All Sides */
.all-example {
    margin: 20px;
}

/* Individual Sides */
.individual-example {
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 20px;
    margin-left: 25px;
}

/* Horizontal and Vertical */
.horizontalVertical-example {
    margin: 10px 20px;
}

/* Auto Margin (centered) */
.auto-example {
    margin: 0 auto;
    width: 50%;
}
```

**HTML:**
```html
<div class="all-example">This div has a 20px margin on all sides.</div>
<div class="individual-example">This div has different margins on each side.</div>
<div class="horizontalVertical-example">This div has 10px vertical and 20px horizontal margins.</div>
<div class="auto-example">This div is centered with auto margins and a width of 50%.</div>
```

<div style="page-break-after: always;"></div>


###  **padding**

**Description:** Specifies the space between the content and the border of an element.

**Usage:**
```css
/* All Sides */
.padding-all-example {
    padding: 20px;
}

/* Individual Sides */
.padding-individual-example {
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 20px;
    padding-left: 25px;
}

/* Horizontal and Vertical */
.padding-horizontalVertical-example {
    padding: 10px 20px;
}
```

**HTML:**
```html
<div class="padding-all-example">This div has a 20px padding on all sides.</div>
<div class="padding-individual-example">This div has different padding on each side.</div>
<div class="padding-horizontalVertical-example">This div has 10px vertical and 20px horizontal padding.</div>
```

<div style="page-break-after: always;"></div>


###  **width**

**Description:** Specifies the width of an element.

**Usage:**
```css
/* Fixed Width */
.width-fixed-example {
    width: 200px;
}

/* Percentage Width */
.width-percentage-example {
    width: 50%;
}
```

**HTML:**
```html
<div class="width-fixed-example">This div has a fixed width of 200px.</div>
<div class="width-percentage-example">This div has a width of 50%.</div>
```

<div style="page-break-after: always;"></div>


### **height**

**Description:** Specifies the height of an element.

**Usage:**
```css
/* Fixed Height */
.height-fixed-example {
    height: 150px;
}

/* Percentage Height */
.height-percentage-example {
    height: 75%;
}
```

**HTML:**
```html
<div class="height-fixed-example">This div has a fixed height of 150px.</div>
<div class="height-percentage-example">This div has a height of 75%.</div>
```

<div style="page-break-after: always;"></div>

###  **border**

**Description:** Specifies the border of an element.

**Usage:**
```css
/* Solid Border */
.border-solid-example {
    border: 1px solid black;
}

/* Dashed Border */
.border-dashed-example {
    border: 2px dashed blue;
}

/* Dotted Border */
.border-dotted-example {
    border: 3px dotted green;
}

/* Double Border */
.border-double-example {
    border: 4px double red;
}
```

**HTML:**
```html
<div class="border-solid-example">This div has a solid border.</div>
<div class="border-dashed-example">This div has a dashed border.</div>
<div class="border-dotted-example">This div has a dotted border.</div>
<div class="border-double-example">This div has a double border.</div>
```

<div style="page-break-after: always;"></div>


### **border-radius**

**Description:** Specifies the radius of the element's corners.

**Usage:**
```css
/* Rounded Corners */
.border-radius-example {
    border: 1px solid black;
    border-radius: 10px;
}

/* Circle */
.circle-example {
    border: 1px solid black;
    border-radius: 50%;
}
```

**HTML:**
```html
<div class="border-radius-example">This div has rounded corners.</div>
<div class="circle-example">This div is a circle.</div>
```


<div style="page-break-after: always;"></div>

### CSS Transformations

CSS `transform` allows you to modify the appearance and position of an element without affecting the layout of other elements.
>[!warning]
> Transform doesn't work on elements with `display: inline;` set.

**Usage:**

#### 1. **Translate**

**Description:** Moves an element along the X and Y axes.

```css
.translate-example {
    transform: translate(50px, 20px);
}
```

**HTML:**
```html
<div class="translate-example">This div is translated 50px right and 20px down.</div>
```

#### 2. **Scale**

**Description:** Changes the size of an element.

```css
.scale-example {
    transform: scale(1.5);
}
```

**HTML:**
```html
<div class="scale-example">This div is scaled to 1.5 times its original size.</div>
```

#### 3. **Rotate**

**Description:** Rotates an element around a fixed point.

```css
.rotate-example {
    transform: rotate(45deg);
}
```

**HTML:**
```html
<div class="rotate-example">This div is rotated 45 degrees clockwise.</div>
```

#### 4. **Transform Origin**

**Description:** Specifies the point around which a transformation should occur.

```css
.transform-origin-example {
    transform-origin: top left;
    transform: rotate(45deg);
}
```

**HTML:**
```html
<div class="transform-origin-example">This div is rotated 45 degrees around its top left corner.</div>
```

---

### Combining Transformations

Transformations can be combined to create more complex effects:

```css
.combine-example {
    transform: translate(50px, 20px) rotate(45deg) scale(1.2);
}
```

```html
<div class="combine-example">This div is translated, rotated, and scaled simultaneously.</div>
```


<div style="page-break-after: always;"></div>


### CSS Transitions

**Description:** CSS transitions allow you to change property values smoothly (over a given duration) between two states.

**Usage:**
```css
.transition-example {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    transition: width 0.3s, height 0.3s, background-color 0.3s;
    /* transition: all 0.3s;*/
}

.transition-example:hover {
    width: 150px;
    height: 150px;
    background-color: lightgreen;
}
```

**HTML:**
```html
<div class="transition-example">Hover over this div to see the transition effect.</div>
```

**Explanation:**
The transition-example div starts with defined properties (`width`, `height`, `background-color`). 
On hover (`:hover`), these properties change smoothly (`transition`) over 0.3 seconds (`0.3s`).

<div style="page-break-after: always;"></div>


### @keyframes Animations

**Description:** `@keyframes` animations define a sequence of keyframes, which describe how an element should change its style over time.

**Usage:**
```css
@keyframes rotate {
    0% {
        transform: rotate(0deg);
    }
    100% {
        transform: rotate(360deg);
    }
}

.animation-example {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    animation: rotate 2s linear infinite;
}
```

**HTML:**
```html
<div class="animation-example"></div>
```

**Explanation:**
- `@keyframes rotate` defines an animation called `rotate`.
- `0%` and `100%` specify the starting and ending points of the animation (`transform: rotate(0deg)` and `transform: rotate(360deg)`).