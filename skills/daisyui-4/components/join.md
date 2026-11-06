### Join
Join is a container for grouping multiple items, such as buttons, inputs, or other elements. Join applies border radius to the first and last item.

[Join documentation](https://v4.daisyui.com/components/join/)

#### Class names
- component: `join`, `join-item`
- modifier: `join-vertical`, `join-horizontal`

#### Syntax
```html
<div class="join">
  <button class="join-item">1</button>
  <button class="join-item">2</button>
</div>
```
#### Rules
- `join-item` is each child; Join applies border radius to the first and last item.
- Use `join-vertical` / `join-horizontal` for orientation.
