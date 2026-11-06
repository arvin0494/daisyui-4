### Accordion
Accordion is used for showing and hiding content but only one item can stay open at a time.

[Accordion documentation](https://v4.daisyui.com/components/accordion/)

#### Class names
- component: `collapse`, `collapse-title`, `collapse-content`
- behavior: `collapse-open`, `collapse-close`
- modifier: `collapse-arrow`, `collapse-plus`

#### Syntax
```html
<div class="collapse collapse-plus">
  <div class="collapse-title">Title</div>
  <div class="collapse-content">Content</div>
</div>
```
#### Rules
- Uses the same `collapse-*` classes as the collapse component, but works with radio inputs so only one item stays open at a time.
- Use different `name` attributes on the hidden radio inputs for each accordion set on the page.
- `collapse-arrow` or `collapse-plus` adds an open/close icon.
