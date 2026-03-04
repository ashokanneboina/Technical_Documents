# 1. Box Model

The **CSS Box Model** explains how every HTML element is displayed on a webpage.

Every element is treated like a **box**.

It has four parts:

* **Content** – The actual text, image, or element.
* **Padding** – Space between the content and the border.
* **Border** – The outline around the padding and content.
* **Margin** – Space outside the border that separates elements from others.

Example idea:
If a div has padding and border, its total size becomes larger than just the content width.

---

# 2. Inline vs Block Elements

HTML elements behave mainly in two ways.

## Block Elements

Block elements take the **full width of the page** and start on a **new line**.

Examples:

* `<div>`
* `<p>`
* `<h1>` to `<h6>`
* `<section>`

Example behavior:

```
<p>Hello</p>
<p>World</p>
```

These appear on **separate lines**.

---

## Inline Elements

Inline elements only take **the space they need** and stay in the **same line**.

Examples:

* `<span>`
* `<a>`
* `<strong>`
* `<img>`

Example:

```
<p>This is <span>inline text</span></p>
```

The text stays in the **same line**.

---

# 3. Positioning (Relative and Absolute)

CSS positioning controls **where elements appear on the page**.

## Relative Position

The element moves **relative to its normal position**.

Example idea:
If you move it `top:10px`, it moves down from where it originally was.

Important point:

* It still keeps its original space in the layout.

---

## Absolute Position

The element is placed **relative to its nearest positioned parent**.

Important points:

* It is **removed from the normal layout flow**
* You can place it anywhere using `top`, `left`, `right`, `bottom`.

Usually the parent has:

```
position: relative
```

and the child has:

```
position: absolute
```

---

# 4. Common CSS Structural Classes

Structural classes help organize the **layout of the page**.

Examples:

**Container**

* Holds the main content
* Often used to center the page

**Row**

* Used to place items horizontally

**Column**

* Used to divide the layout into sections

**Header**

* Top part of the website (logo, navigation)

**Footer**

* Bottom part of the website (copyright, links)

These classes help build the **structure of the webpage**.

---

# 5. Common CSS Styling Classes

Styling classes control the **appearance of elements**.

Examples:

**Text styling**

* `text-center` → center text
* `text-bold` → bold text

**Colors**

* `bg-primary` → background color
* `text-white` → white text

**Spacing**

* `margin-top`
* `padding`

These classes change **how elements look**, not their structure.

---

# 6. CSS Specificity

CSS Specificity decides **which CSS rule is applied** if multiple rules target the same element.

Priority order:

1. Inline styles
2. ID selectors
3. Class selectors
4. Element selectors

Example idea:

If an element has both **ID and class styles**, the **ID style will override the class style**.

This is called **CSS specificity priority**.

---

# 7. CSS Responsive Queries (Media Queries)

Responsive design means the website works well on **mobile, tablet, and desktop screens**.

**Media queries** allow CSS to change based on screen size.

Example idea:

When the screen is small (mobile), the layout changes to fit the screen.

Common uses:

* Change layout
* Resize images
* Stack elements vertically

This helps create **mobile-friendly websites**.

---

# 8. Flexbox

Flexbox is a layout system used to **arrange items in a row or column easily**.

Key idea:
A **flex container** controls its **flex items**.

Common features:

* Align items horizontally
* Align items vertically
* Distribute space between items

Benefits:

* Easy alignment
* Responsive layouts
* Less complicated than older layout methods

Flexbox works best for **one-direction layouts (row or column).**

---

# 9. CSS Grid

CSS Grid is a layout system used to create **rows and columns at the same time**.

It is useful for **complex page layouts**.

Example idea:
You can divide the page into **multiple columns and rows like a grid**.

Benefits:

* More control over layout
* Easy to create complex designs
* Good for full page layouts

Grid works in **two dimensions (rows and columns).**

---

# 10. Common Header Meta Tags

Meta tags provide **information about the webpage** to browsers and search engines.

Important meta tags:

**Charset**

```
<meta charset="UTF-8">
```

Defines the character encoding.

**Viewport**

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Makes the website responsive on mobile devices.

**Description**
Provides a short description of the webpage.

**Author**
Specifies the author of the page.

**Keywords**
Helps search engines understand the page topic.

---

# 11. Other Important CSS Topics

Some additional useful CSS concepts:

**Z-index**

* Controls which element appears on top of others.

**Overflow**

* Controls what happens when content is larger than its container.

**CSS Variables**

* Store reusable values like colors or spacing.

These features help make CSS **more flexible and easier to manage**.

---

# References

1. Mozilla Developer Network (MDN) – [https://developer.mozilla.org](https://developer.mozilla.org)
2. W3Schools CSS Tutorial – [https://www.w3schools.com/css](https://www.w3schools.com/css)
