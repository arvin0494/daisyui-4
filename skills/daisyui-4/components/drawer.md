### Drawer
Drawer is a grid layout that can show/hide a sidebar on the left or right side of the page.

[Drawer documentation](https://v4.daisyui.com/components/drawer/)

#### Class names
- component: `drawer`, `drawer-toggle`, `drawer-content`, `drawer-side`, `drawer-overlay`
- behavior: `drawer-open`
- modifier: `drawer-end`

#### Syntax
```html
<div class="drawer">
  <input id="my-drawer" type="checkbox" class="drawer-toggle" />
  <div class="drawer-content">Content</div>
  <div class="drawer-side">Sidebar</div>
</div>
```
#### Rules
- `drawer-toggle` is a hidden checkbox that opens the sidebar on mobile.
- `drawer-side` holds the sidebar; `drawer-content` holds the main content. Use `drawer-end` for a right sidebar.
