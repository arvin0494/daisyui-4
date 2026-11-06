---
name: daisyui-4-install
description: Installation instructions for daisyUI 4 (Tailwind CSS 3)
---

## Install daisyUI 4
[Installation guide](https://v4.daisyui.com/docs/install/)
daisyUI 4 requires **Tailwind CSS 3**. Do not use daisyUI 4 with Tailwind CSS 4.

1. You must use Tailwind CSS 3 with daisyUI 4.
2. Install daisyUI as a dev dependency, then add it to `tailwind.config.js`:
```js
module.exports = {
  //...
  plugins: [
    require('daisyui'),
  ],
}
```
or with an ESM import:
```js
import daisyui from "daisyui"
export default {
  //...
  plugins: [daisyui],
}
```
3. Install daisyUI as a dependency when possible. If you have a specific reason to use a CDN instead, use the daisyUI v4 CSS file and the Tailwind CSS 3 Play CDN:
```html
<link href="https://cdn.jsdelivr.net/npm/daisyui@4.12.24/dist/full.min.css" rel="stylesheet" type="text/css" />
<script src="https://cdn.tailwindcss.com"></script>
```
4. If Tailwind CSS and daisyUI are Node.js dependencies, add daisyUI to `tailwind.config.js` as shown above, and make sure your CSS entry includes the Tailwind directives (`@tailwind base; @tailwind components; @tailwind utilities;`).

### CDN

For a browser setup with no installation, load the precompiled daisyUI CSS and the Tailwind CSS 3 Play CDN:

```html
<link href="https://cdn.jsdelivr.net/npm/daisyui@4.12.24/dist/full.min.css" rel="stylesheet" type="text/css" />
<script src="https://cdn.tailwindcss.com"></script>
```

- Use the full file path. `https://cdn.jsdelivr.net/npm/daisyui@4` serves the package JavaScript entry, not CSS, and `https://cdn.jsdelivr.net/npm/tailwindcss@3` is the Node.js build, not a browser script.
- `dist/full.min.css` contains every component and all 32 built-in themes (about 2.9 MB). For production, build the CSS with the Tailwind CLI so unused styles are purged.
- `https://cdn.jsdelivr.net/npm/daisyui@4.12.24/dist/themes.css` contains only the theme variables. It does not replace `full.min.css`.
- The CDN files do not include the `is-drawer-open:` and `is-drawer-close:` variants. Those variants exist only in daisyUI 5.

### Standalone and framework-specific setup

- If you use the Tailwind CSS standalone executable without Node.js, use the [standalone guide](https://v4.daisyui.com/docs/install/standalone/).
- For other installations, select the guide for the applicable framework or build tool:
  [11ty](https://v4.daisyui.com/docs/install/11ty/),
  [Angular](https://v4.daisyui.com/docs/install/angular/),
  [Astro](https://v4.daisyui.com/docs/install/astro/),
  [Bun](https://v4.daisyui.com/docs/install/bun/),
  [Tailwind CLI](https://v4.daisyui.com/docs/install/cli/),
  [Django](https://v4.daisyui.com/docs/install/django/),
  [Electron](https://v4.daisyui.com/docs/install/electron/),
  [Ember](https://v4.daisyui.com/docs/install/ember/),
  [Fresh](https://v4.daisyui.com/docs/install/fresh/),
  [HTMX](https://v4.daisyui.com/docs/install/htmx/),
  [Laravel](https://v4.daisyui.com/docs/install/laravel/),
  [Lit](https://v4.daisyui.com/docs/install/lit/),
  [Next.js](https://v4.daisyui.com/docs/install/nextjs/),
  [Nuxt](https://v4.daisyui.com/docs/install/nuxt/),
  [Phoenix](https://v4.daisyui.com/docs/install/phoenix/),
  [PostCSS](https://v4.daisyui.com/docs/install/postcss/),
  [Preact](https://v4.daisyui.com/docs/install/preact/),
  [Qwik](https://v4.daisyui.com/docs/install/qwik/),
  [Rails](https://v4.daisyui.com/docs/install/rails/),
  [React](https://v4.daisyui.com/docs/install/react/),
  [React Router](https://v4.daisyui.com/docs/install/reactrouter/),
  [SvelteKit](https://v4.daisyui.com/docs/install/sveltekit/),
  [Tailscan](https://v4.daisyui.com/docs/install/tailscan/),
  [UnoCSS](https://v4.daisyui.com/docs/install/unocss/),
  [Vike](https://v4.daisyui.com/docs/install/vike/),
  [Vite](https://v4.daisyui.com/docs/install/vite/),
  [Vue](https://v4.daisyui.com/docs/install/vue/),
  [WordPress](https://v4.daisyui.com/docs/install/wordpress/), or
  [Zola](https://v4.daisyui.com/docs/install/zola/).

Use the file paths and integration steps in the selected guide. Each framework can use a different CSS entry.
