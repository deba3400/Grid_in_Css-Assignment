In CSS Grid Layout, `grid-auto-row` and `grid-auto-column` are properties used to define the size, behavior, and alignment of grid tracks that are created automatically to accommodate grid items that do not explicitly occupy a grid cell. These properties allow you to control the sizing and alignment of these implicitly generated rows and columns.

Here's an explanation with examples for both properties:

### grid-auto-row:

`grid-auto-row` is used to specify the size and behavior of implicitly created rows in a grid container.

#### Example:

```css
.grid-container {
  display: grid;
  grid-template-columns: 100px 100px;
  grid-auto-rows: 50px; 
}

.grid-item {
  background-color: lightblue;
}
```

```html
<div class="grid-container">
  <div class="grid-item">Item 1</div>
  <div class="grid-item">Item 2</div>
  <div class="grid-item">Item 3</div>
  <div class="grid-item">Item 4</div>
  <div class="grid-item">Item 5</div>
</div>
```

In this example, the grid container has explicitly defined two columns of 100px each. However, the rows are generated implicitly. The `grid-auto-rows` property sets the height of these automatically generated rows to 50px each. Therefore, any grid items beyond the second one will be placed in a new row, each row being 50px in height.

### grid-auto-column:

`grid-auto-column` is used to specify the size and behavior of implicitly created columns in a grid container.

#### Example:

```css
.grid-container {
  display: grid;
  grid-template-rows: 100px 100px;
  grid-auto-columns: 50px; 
}

.grid-item {
  background-color: lightblue;
}
```

```html
<div class="grid-container">
  <div class="grid-item">Item 1</div>
  <div class="grid-item">Item 2</div>
  <div class="grid-item">Item 3</div>
  <div class="grid-item">Item 4</div>
  <div class="grid-item">Item 5</div>
</div>
```

In this example, the grid container has explicitly defined two rows of 100px each. However, the columns are generated implicitly. The `grid-auto-columns` property sets the width of these automatically generated columns to 50px each. Therefore, any grid items beyond the second one will be placed in a new column, each column being 50px in width.

These properties are particularly useful when dealing with grid layouts where the number of items is dynamic or unknown beforehand, allowing you to control the layout of additional rows and columns as needed.