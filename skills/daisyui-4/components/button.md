### Button
Buttons allow the user to take actions or make choices.

[Button documentation](https://v4.daisyui.com/components/button/)

#### Class names
- component: `btn`
- color: `btn-neutral`, `btn-primary`, `btn-secondary`, `btn-accent`, `btn-info`, `btn-success`, `btn-warning`, `btn-error`
- style: `btn-ghost`, `btn-link`, `btn-outline`, `glass`
- behavior: `btn-active`, `btn-disabled`
- size: `btn-lg`, `btn-md`, `btn-sm`, `btn-xs`
- modifier: `no-animation`, `btn-wide`, `btn-block`, `btn-circle`, `btn-square`

#### Syntax
```html
<button class="btn">Button</button>
```
#### Rules
- Use `btn` on `<button>`, `<a>`, or `<input>`.
- Add one color (`btn-primary`), one style (`btn-outline`, `btn-ghost`, `btn-link`), one size (`btn-lg`), and one modifier (`btn-wide`, `btn-square`, `btn-circle`).
- To disable with a class, also add `tabindex="-1" role="button" aria-disabled="true"`.
