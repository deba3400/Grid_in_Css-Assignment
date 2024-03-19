In CSS Grid and Flexbox layouts, both `justify-items` and `justify-self` properties are used to control the alignment of items along the inline (main) axis. However, they apply to different levels of the layout hierarchy.

### justify-items:

`justify-items` is a property used in a grid or flex container to define how the items inside that container should be aligned along the inline axis by default.

#### Example:

```css
.container {
  display: grid;
  grid-template-columns: 100px 100px;
  justify-items: center;
}

.item {
  background-color: lightblue;
}
```

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```

In this example, `justify-items: center;` aligns the items along the inline axis (horizontally in this case, since it's a grid layout) to the center of each grid cell. This alignment applies to all items within the grid container unless overridden by individual item properties.

### justify-self:

`justify-self` is a property used in a grid or flex item to define how that particular item should be aligned along the inline axis within its container.

#### Example:

```css
.item {
  background-color: lightblue;
  justify-self: end;
}
```

```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
</div>
```

In this example, `justify-self: end;` aligns each item individually along the inline axis (horizontally in this case) to the end of its grid cell. This overrides the default alignment set by `justify-items` for these specific items.

### Summary:

- `justify-items` is used at the container level to define the default alignment of all items within that container.
- `justify-self` is used at the item level to override the default alignment set by `justify-items` for that specific item.

In essence, `justify-items` sets the default alignment for all items in a container, while `justify-self` allows you to individually adjust the alignment of specific items within that container.