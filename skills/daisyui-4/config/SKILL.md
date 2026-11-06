---
name: daisyui-4-config
description: Configuration options for daisyUI 4 (Tailwind CSS 3)
---

## Configuration
daisyUI 4 is configured from `tailwind.config.js`, not from a CSS file. daisyUI configuration documentation: https://v4.daisyui.com/docs/config/

Add daisyUI and configure it in `tailwind.config.js`:
```js
module.exports = {
  //...
  plugins: [require("daisyui")],
  daisyui: {
    // options:
    themes: ["light", "dark"],
    darkTheme: "dark",
    base: true,
    styled: true,
    utils: true,
    prefix: "",
    logs: true,
    themeRoot: ":root",
  },
}
```

### A minimal configuration with only the `light` theme
```js
module.exports = {
  plugins: [require("daisyui")],
  daisyui: {
    themes: ["light"],
  },
}
```

### Config values explained
- `styled` (Boolean, default true): If true, components have colors and style. If false, components have no color or style so you can design your own skeleton.
- `themes` (Boolean or array, default false): `true` includes all themes. `false` includes only light and dark. An array includes only the listed themes, and the first theme is the default.
- `base` (Boolean, default true): If true, a few base styles set the page background and foreground colors.
- `utils` (Boolean, default true): If true, responsive and modifier utility classes are added.
- `logs` (Boolean, default true): If true, daisyUI logs its version and config to the terminal while building CSS.
- `darkTheme` (String, default "dark"): The theme used for the system dark mode.
- `prefix` (String, default ""): A prefix added to all daisyUI class names to avoid conflicts with another library.
- `themeRoot` (String, default ":root"): The element that receives the theme CSS variables.

### Enable every built-in theme
This configuration enables all built-in themes. The first theme is the default. To use another enabled theme, add `data-theme="THEME_NAME"` to the `<html>` element.
```js
module.exports = {
  plugins: [require("daisyui")],
  daisyui: {
    themes: [
      "light","dark","cupcake","bumblebee","emerald","corporate","synthwave",
      "retro","cyberpunk","valentine","halloween","garden","forest","aqua",
      "lofi","pastel","fantasy","wireframe","black","luxury","dracula","cmyk",
      "autumn","business","acid","lemonade","night","coffee","winter","dim",
      "nord","sunset",
    ],
  },
}
```

### Use a prefix and disable logs
```js
module.exports = {
  plugins: [require("daisyui")],
  daisyui: {
    themes: ["light", "dark"],
    prefix: "daisy-",
    logs: false,
  },
}
```
