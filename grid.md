

# CSS Grid

**CSS Grid** is a layout system used to create **two-dimensional layouts (rows and columns)** to arrange elements on a webpage.

A **grid container** holds **grid items**, which are placed inside **grid cells formed by rows and columns**.

---

# 1. Grid Structure 

Properties that **create the grid layout**.

### Properties

* `display`
* `grid-template-columns`
* `grid-template-rows`
* `gap`

### Example

```css
.container{
  display:grid;
  grid-template-columns:200px 1fr;
  grid-template-rows:100px 200px;
  gap:10px;
}
```

Explanation
Creates **2 columns and 2 rows** with spacing between cells.

---

# 2. Aligning the Entire Grid

These align the **whole grid inside the container**.

### Properties

* `justify-content`
* `align-content`
* `place-content`

Values commonly used:

```
start
end
center
space-between
space-around
space-evenly
stretch
```

### Example

```css
.container{
  display:grid;
  grid-template-columns:100px 100px;
  height:400px;

  justify-content:center;
  align-content:center;
}
```

The **entire grid moves to the center of the container**.



---

# 3. Aligning Items Inside Grid Cells

These control **alignment of items inside their individual cells**.

### Properties

* `justify-items` → horizontal alignment
* `align-items` → vertical alignment
* `place-items` → shortcut for both

### Example

```css
.container{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  height:200px;

  justify-items:center;
  align-items:center;
}
```

Items appear **centered inside each cell**.

---

# 4. Aligning Individual Grid Items

These align **a single item inside its cell**.

### Properties

* `justify-self`
* `align-self`

### Example

```css
.item{
  justify-self:center;
  align-self:center;
}
```

The specific item becomes **centered inside its grid cell**.

---

# 5. Positioning Grid Items

These properties **control where items appear in the grid**.

### Properties

* `grid-column`
* `grid-row`
* `grid-area`

### Example

```css
.box1{
  grid-column:1 / 3;
}

.box2{
  grid-row:1 / 3;
}
```

* `grid-column:1/3` → spans **two columns**
* `grid-row:1/3` → spans **two rows**
* `grid-area: 1 / 1 / 3 / 3` → **row-start / column-start / row-end / column-end**
---

# 6. Layout Using Named Areas

Helps create **readable page layouts**.

### Properties

* `grid-template-areas`
* `grid-area`

### Example

```css
.container{
  display:grid;
  grid-template-columns:200px 1fr;

  grid-template-areas:
  "header header"
  "sidebar content";
}

.header{ grid-area:header; }
.sidebar{ grid-area:sidebar; }
.content{ grid-area:content; }
```

Layout becomes:

```
header   header
sidebar  content
```

---

# Important Grid Functions

### `repeat()`

Repeats row or column definitions.

```
grid-template-columns: repeat(3,1fr);
```

Creates **3 equal columns**.

---

### `minmax()`

Defines **minimum and maximum size for a row or column**.

```
grid-template-columns: minmax(100px,300px);
```

Column size stays **between 100px and 300px**.

---

# Combined Example

### HTML

```html
<div class="container">
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Content</div>
</div>
```

### CSS

```css
.container{
  display:grid;

  grid-template-columns:200px 1fr;
  grid-template-rows:80px 200px;

  grid-template-areas:
  "header header"
  "sidebar content";

  gap:10px;

  place-items:center;
  justify-content:center;
}

.header{ grid-area:header; background:lightblue; }
.sidebar{ grid-area:sidebar; background:lightgreen; }
.content{ grid-area:content; background:lightcoral; }
```
