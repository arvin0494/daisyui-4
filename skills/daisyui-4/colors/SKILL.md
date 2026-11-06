---
name: daisyui-4-colors
description: Color rules that you must use with daisyUI 4 (Tailwind CSS 3)
---

## daisyUI 4 colors

### daisyUI color names
- `primary`: The main brand color.
- `primary-content`: Foreground content color for use on `primary`.
- `secondary`: An optional secondary brand color.
- `secondary-content`: Foreground content color for use on `secondary`.
- `accent`: An optional accent brand color.
- `accent-content`: Foreground content color for use on `accent`.
- `neutral`: A dark neutral color for UI areas that do not use saturated colors.
- `neutral-content`: Foreground content color for use on `neutral`.
- `base-100`: The page base-surface color for blank backgrounds.
- `base-200`: A darker base shade that gives elevation.
- `base-300`: A still darker base shade that gives more elevation.
- `base-content`: Foreground content color for use on a base color.
- `info`: Color for information and help messages.
- `info-content`: Foreground content color for use on `info`.
- `success`: Color for success and safe-state messages.
- `success-content`: Foreground content color for use on `success`.
- `warning`: Color for warning and caution messages.
- `warning-content`: Foreground content color for use on `warning`.
- `error`: Color for error, danger, and destructive-action messages.
- `error-content`: Foreground content color for use on `error`.

### daisyUI color rules
1. daisyUI adds semantic color names to the Tailwind CSS colors.
2. Use daisyUI color names in utility classes as you use other Tailwind CSS color names. For example, `bg-primary` uses the primary color for the background.
3. The value of each daisyUI color name is a variable. Thus, the color can change with the theme.
4. Do not use `dark:` with daisyUI color names.
5. If possible, use only daisyUI color names. This lets colors change automatically with the theme.
6. If you use a Tailwind CSS color name such as `red-500`, its color stays the same in all themes.
7. If you use a daisyUI color name such as `primary`, its color changes with the theme.
8. Avoid Tailwind CSS color names for text. For example, `text-gray-800` on `bg-base-100` becomes unreadable in a dark theme because `bg-base-100` is dark.
9. `*-content` colors must have clear contrast with their related colors.
10. Use `base-*` colors for most of the page. Use the default variant for all elements. Use `primary` only for the most important element on the page. Use it only once.
11. In rare cases, you can use a Tailwind CSS color if content must keep the same color in all themes. For example, you can use `text-red-500` instead of `text-error`. For an SVG icon or chart, a fixed color can be necessary.

### Enable and apply themes
Themes are configured in `tailwind.config.js`. In the daisyUI config, select specified themes, all themes, or no built-in themes:

```js
module.exports = {
  plugins: [require("daisyui")],
  daisyui: {
    themes: ["light", "dark", "cupcake"],
  },
}
```

- Use `themes: true` to enable all built-in themes.
- Use `themes: false` to disable all built-in themes except the default light and dark.
- Use `themes: []` to disable all themes and colors.
- Add `data-theme="THEME_NAME"` to `<html>` or a nested element. You can nest themes with no depth limit.

```html
<html data-theme="dark">
  <section data-theme="light">
    <div data-theme="retro">Nested theme</div>
  </section>
</html>
```

### daisyUI custom theme (colors in tailwind.config.js)
Define a custom theme in `tailwind.config.js`. Only the required colors are needed; daisyUI generates the rest. Optional CSS-variable design decisions can be added too.

```js
module.exports = {
  plugins: [require("daisyui")],
  daisyui: {
    themes: [
      {
        mytheme: {
          primary: "#a991f7",
          secondary: "#f6d860",
          accent: "#37cdbe",
          neutral: "#3d4451",
          "base-100": "#ffffff",
        },
      },
      "dark",
      "cupcake",
    ],
  },
}
```

Optional design-decision variables:
```js
{
  mytheme: {
    primary: "#a991f7",
    secondary: "#f6d860",
    accent: "#37cdbe",
    neutral: "#3d4451",
    "base-100": "#ffffff",

    "--rounded-box": "1rem", // border radius of boxes (card, modal, alert)
    "--rounded-btn": "0.5rem", // border radius of buttons
    "--rounded-badge": "1.9rem", // border radius of badges
    "--animation-btn": "0.25s", // button click animation duration
    "--animation-input": "0.2s", // input animation duration
    "--btn-focus-scale": "0.95", // button focus scale
    "--border-btn": "1px", // button border width
    "--tab-border": "1px", // tab border width
    "--tab-radius": "0.5rem", // tab border radius
  },
}
```

- Colors can use hex, OKLCH, or another format.
- If you generate a custom theme, do not include the comments. Give only the code.

Optional: Use the visual tool at https://v4.daisyui.com/theme-generator/ to make a custom theme.

### Change an existing theme
Require an existing daisyUI theme and override some colors in `tailwind.config.js`:
```js
daisyui: {
  themes: [
    {
      light: {
        ...require("daisyui/src/theming/themes")["light"],
        primary: "blue",
        secondary: "teal",
      },
    },
  ],
}
```

### Apply Tailwind's `dark:` selector to a specific theme
```js
module.exports = {
  plugins: [require("daisyui")],
  daisyui: {
    themes: ["winter", "night"],
  },
  darkMode: ["selector", "[data-theme=\"night\"]"],
}
```
