### Modal
Modal is used to show a dialog or a box when you click a button.

[Modal documentation](https://v4.daisyui.com/components/modal/)

#### Class names
- component: `modal`, `modal-box`, `modal-action`, `modal-backdrop`, `modal-toggle`
- behavior: `modal-open`
- modifier: `modal-top`, `modal-bottom`, `modal-middle`

#### Syntax
```html
<div class="modal" id="my-modal">
  <div class="modal-box">
    <div class="modal-action"><a class="btn" href="#my-modal">Close</a></div>
  </div>
</div>
```
#### Rules
- Three methods: a `<dialog>` element (recommended), a hidden checkbox + `modal-toggle`, or anchor links.
- Structure: `modal` > `modal-box` > content + `modal-action`. Add `modal-backdrop` for a click-outside-to-close backdrop.
- Use `modal-open` to open/close with JS, and `modal-top` / `modal-bottom` / `modal-middle` for position.
