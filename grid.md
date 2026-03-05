## CSS Grid

**CSS Grid** is a layout system used to create **two-dimensional layouts (rows and columns)** for arranging elements on a webpage.
The **grid container** holds **grid items**, which are placed inside **grid cells formed by rows and columns**.

---

# 1. Grid Container (Basic Structure)

These properties **create the grid structure**.

### Properties

* **`display`** → activates grid layout
* **`grid-template-columns`** → defines number and width of columns
* **`grid-template-rows`** → defines number and height of rows
* **`gap`** → space between grid cells

### Example

```css
.container{
  display: grid;
  grid-template-columns: 200px 1fr;
  grid-template-rows: 100px 100px;
  gap: 10px;
}
```

Explanation:

* Grid becomes **2 columns and 2 rows**
* `200px` column + flexible column (`1fr`)
* `gap` creates spacing between cells

---

# 2. Item Alignment (Inside Cells)

These properties **align grid items inside their cells**.

### Properties

* **`justify-items`** → horizontal alignment
* **`align-items`** → vertical alignment
* **`place-items`** → shortcut for both

Values commonly used:

```
start
end
center
stretch
```

### Example

```css
.container{
  display: grid;
  grid-template-columns: repeat(2,1fr);
  height: 200px;
  justify-items: center;
  align-items: center;
}
```

Explanation:

* Items are **centered horizontally and vertically inside each grid cell**.

---

# 3. Grid Placement (Positioning Items)

These properties **control where items appear in the grid**.

### Properties

* **`grid-column`** → controls column span
* **`grid-row`** → controls row span
* **`grid-area`** → shortcut for row + column placement

### Example

```css
.box1{
  grid-column: 1 / 3;
}

.box2{
  grid-row: 1 / 3;
}
```

Explanation:

* `grid-column:1/3` → item spans **two columns**
* `grid-row:1/3` → item spans **two rows**

---

# 4. Layout Using Named Areas

These properties help **create readable layouts**.

### Properties

* **`grid-template-areas`** → defines layout structure
* **`grid-area`** → assigns items to those areas

### Example

```css
.container{
  display:grid;
  grid-template-columns:200px 1fr;
  grid-template-areas:
  "header header"
  "sidebar content";
}

.header{
  grid-area: header;
}

.sidebar{
  grid-area: sidebar;
}

.content{
  grid-area: content;
}
```

Explanation:

* Layout becomes

```
header   header
sidebar  content
```

---

# Important Grid Functions

### `repeat()`

Repeats column or row definitions.

```css
grid-template-columns: repeat(3,1fr);
```

Creates **3 equal columns**.

### `minmax()`

Defines minimum and maximum size of a grid track.

```css
grid-template-columns: minmax(100px,300px);
```

Column size stays **between 100px and 300px**.

---

# Complete Working Example

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
}

.header{ grid-area:header; background:lightblue; }
.sidebar{ grid-area:sidebar; background:lightgreen; }
.content{ grid-area:content; background:lightcoral; }
```

Layout:

```
+----------------------+
|        HEADER        |
+-----------+----------+
| SIDEBAR   | CONTENT  |
+-----------+----------+
```

