### Dropdown
Dropdown can open a menu or any other element when the button is clicked.

[Dropdown documentation](https://v4.daisyui.com/components/dropdown/)

#### Class names
- component: `dropdown`, `dropdown-content`
- behavior: `dropdown-hover`, `dropdown-open`
- modifier: `dropdown-end`, `dropdown-top`, `dropdown-bottom`, `dropdown-left`, `dropdown-right`

#### Syntax
```html
<div class="dropdown">
  <div tabindex="0" role="button" class="btn">Open</div>
  <ul tabindex="0" class="dropdown-content menu">Items</ul>
</div>
```
#### Rules
- A `tabindex="0" role="button"` trigger opens the `dropdown-content`.
- Add `dropdown-end` to align right, `dropdown-hover` for hover open, and `dropdown-open` to force open.
