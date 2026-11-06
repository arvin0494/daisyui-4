### Theme Controller
If a checked checkbox or radio input with the theme-controller class exists on the page, the page will use the same theme as that input's value.

[Theme Controller documentation](https://v4.daisyui.com/components/theme-controller/)

#### Class names
- component: `theme-controller`

#### Syntax
```html
<input type="checkbox" class="theme-controller" value="dark" />
```
#### Rules
- A checked checkbox/radio with `theme-controller` and a theme name in its `value` sets the page theme.
- This uses the CSS `:has()` selector (Chrome 105+, Firefox 121+, Safari 15.4+). Firefox 115 ESR does not support it. On those browsers, set `data-theme` on `<html>` with JavaScript instead.
