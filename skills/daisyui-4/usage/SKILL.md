---
name: daisyui-4-usage
description: Usage rules that you must use with daisyUI 4 (Tailwind CSS 3)
---

## daisyUI 4 usage rules
1. To style an HTML element, add daisyUI class names to it. Add the necessary component class name. Also add the applicable part and modifier class names.
2. If the current daisyUI classes cannot make a necessary change, use Tailwind CSS utility classes. For example, `btn px-10` sets custom horizontal padding on a `btn`.
3. If CSS specificity prevents a change to a daisyUI style, add `!` before the Tailwind utility (Tailwind CSS 3 syntax). For example, `btn !bg-red-500` overrides the background color of a `btn`. Use this method only if other methods do not work. Do not use it frequently.
4. If daisyUI does not have an applicable component, make a component with Tailwind CSS utilities.
5. When you use Tailwind CSS `flex` or `grid` for a layout, add responsive utility prefixes.
6. Use only current daisyUI class names or Tailwind CSS utility classes.
7. If custom CSS is not necessary, do not write it. If possible, use daisyUI class names or Tailwind CSS utility classes.
8. If you need placeholder images, use https://picsum.photos/200/300 with the necessary dimensions.
9. If a custom font is not necessary, do not add one.
10. If `bg-base-100 text-base-content` is not necessary, do not add it to the body.
11. For design decisions, use the methods in the Refactoring UI book.
12. If the user does not request a variant or color, use the default variant. For example, use `btn` for a button. If the user does not request that variant, do not use `btn btn-primary`.

Each daisyUI 4 class name is in one of these categories. These category names are for reference only. Do not use them in code.
- `component`: The necessary component class, and child-part classes such as `card-body`.
- `color`: Sets a specified color on a component or part.
- `style`: Sets a specified style on a component or part.
- `behavior`: Changes the behavior of a component or part.
- `size`: Sets a specified size on a component or part.
- `placement`: Sets a specified position for a component or part.
- `direction`: Sets a specified direction for a component or part.
- `modifier`: Changes the component or part in a specified way.
- `variant`: A prefix that applies styles under a condition. In daisyUI 4 the responsive classes (for example `btn-lg`) are applied without a breakpoint prefix; use Tailwind's own responsive prefixes such as `sm:` for breakpoints.

## Change a component in CSS

daisyUI 4 runs on Tailwind CSS 3. To change a daisyUI component globally, use the Tailwind `@apply` directive inside a class in your CSS file:

```css
.btn {
  @apply rounded-full;
}
```

## daisyUI utilities and variables

- You can use semantic colors with Tailwind color utilities and opacity modifiers. Examples are `bg-primary`, `border-base-300`, and `text-base-content/60`.
- `rounded-box`, `rounded-btn`, and `rounded-badge` use the radius tokens of the active theme.
- `glass` applies the daisyUI glass effect.
- Some components supply CSS variables for component-specific changes. Countdown uses `--value` and `--digits`. Radial progress uses `--size` and `--thickness`.
