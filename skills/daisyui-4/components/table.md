### Table
Table can be used to show a list of data in a table format.

[Table documentation](https://v4.daisyui.com/components/table/)

#### Class names
- component: `table`
- size: `table-xs`, `table-sm`, `table-md`, `table-lg`
- modifier: `table-zebra`, `table-pin-rows`, `table-pin-cols`

#### Syntax
```html
<table class="table">
  <tr><th>A</th><th>B</th></tr>
</table>
```
#### Rules
- Use `<tr>` rows inside `<tbody>`, `table-zebra` for striped rows, and `table-{size}` for size.
- Use `table-pin-rows` / `table-pin-cols` to freeze rows/columns.
