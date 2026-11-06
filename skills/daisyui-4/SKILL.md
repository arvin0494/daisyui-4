---
name: daisyui-4
description: daisyUI 4 component-library skill for Tailwind CSS 3. Use it when you write HTML or JSX code in a project that uses daisyUI 4. Even if the user does not request it, use it.
metadata:
  version: 4.12.x
  source: https://v4.daisyui.com/docs/
---

# daisyUI 4
daisyUI 4 is a CSS library for **Tailwind CSS 3**. It supplies class names for common UI components, semantic colors, and themes.

> This skill is for **daisyUI 4 with Tailwind CSS 3**. If the project uses **daisyUI 5 with Tailwind CSS 4**, use the `daisyui` skill instead. The two versions differ in installation, configuration, and some class names.

## Target browsers: Firefox 115 ESR on Windows 7

Assume browsers as old as **Firefox 115 ESR** (the last Firefox version for Windows 7) unless the project says otherwise. daisyUI 4 and Tailwind CSS 3 output plain CSS that these browsers support. These features do not work:

- `:has()` (Firefox 121+). daisyUI 4 uses it only in `theme-controller`. On older browsers, set `data-theme` on `<html>` with JavaScript.
- CSS nesting (Firefox 117+). Write flat selectors.
- `text-wrap: balance` (Firefox 121+). Do not use the Tailwind `text-balance` utility.
- `light-dark()` (Firefox 120+), `@property` (Firefox 128+), and relative color syntax such as `rgb(from ...)` (Firefox 128+).
- `color-mix()` and `oklch()` work (Firefox 113+), so the built-in theme colors are safe.

Tailwind CSS 4 and daisyUI 5 require Firefox 128+. Do not upgrade the project to them if these browsers must work.

## When to use this skill

- Use this skill each time you write HTML or JSX code.
- Use this skill for all Tailwind CSS UI work in a daisyUI 4 project.
- If the user uses one of these terms or requests related work, use this skill:
  daisyUI, component, UI, Tailwind, layout, template, theme, color, design
- Even if the user does not request this skill, use it.

## References that you must read

| Task | Guide | Note |
|------|-------|------|
Install daisyUI | [./install/SKILL.md](./install/SKILL.md) | If the project does not have daisyUI, use this guide.
Use daisyUI class names | [./usage/SKILL.md](./usage/SKILL.md) | You must read this guide before you use daisyUI class names in code.
Configure daisyUI | [./config/SKILL.md](./config/SKILL.md) | Read this guide to configure themes, prefixes, logs, or other options. You do not need it for basic use.
daisyUI colors and themes | [./colors/SKILL.md](./colors/SKILL.md) | You must read this guide before you use daisyUI colors in code.
daisyUI components | [./components/](./components/) | You must read the applicable component guides before you use daisyUI components. Read more than one candidate guide before you select a component.

## List of components

- [accordion](./components/accordion.md)
- [alert](./components/alert.md)
- [artboard](./components/artboard.md)
- [avatar](./components/avatar.md)
- [badge](./components/badge.md)
- [bottom navigation](./components/bottom-navigation.md)
- [breadcrumbs](./components/breadcrumbs.md)
- [button](./components/button.md)
- [card](./components/card.md)
- [carousel](./components/carousel.md)
- [chat](./components/chat.md)
- [checkbox](./components/checkbox.md)
- [collapse](./components/collapse.md)
- [countdown](./components/countdown.md)
- [diff](./components/diff.md)
- [divider](./components/divider.md)
- [drawer](./components/drawer.md)
- [dropdown](./components/dropdown.md)
- [file input](./components/file-input.md)
- [footer](./components/footer.md)
- [hero](./components/hero.md)
- [indicator](./components/indicator.md)
- [input](./components/input.md)
- [join (group)](./components/join.md)
- [kbd](./components/kbd.md)
- [link](./components/link.md)
- [loading](./components/loading.md)
- [mask](./components/mask.md)
- [menu](./components/menu.md)
- [mockup browser](./components/mockup-browser.md)
- [mockup code](./components/mockup-code.md)
- [mockup phone](./components/mockup-phone.md)
- [mockup window](./components/mockup-window.md)
- [modal](./components/modal.md)
- [navbar](./components/navbar.md)
- [pagination](./components/pagination.md)
- [progress](./components/progress.md)
- [radial progress](./components/radial-progress.md)
- [radio](./components/radio.md)
- [range](./components/range.md)
- [rating](./components/rating.md)
- [select](./components/select.md)
- [skeleton](./components/skeleton.md)
- [stack](./components/stack.md)
- [stat](./components/stat.md)
- [steps](./components/steps.md)
- [swap](./components/swap.md)
- [tab](./components/tab.md)
- [table](./components/table.md)
- [textarea](./components/textarea.md)
- [theme controller](./components/theme-controller.md)
- [timeline](./components/timeline.md)
- [toast](./components/toast.md)
- [toggle (switch)](./components/toggle.md)
- [tooltip](./components/tooltip.md)

### Component discovery protocol

Before you write daisyUI code, do these steps in sequence:

1. Identify the intended function, behavior, and layout in the request. Do not use only the exact words.
2. Use the component list in this file to select the best candidate components.
3. If the choice is not clear, read the guides for the candidate components that can meet the request before you select one.
4. Compare the description, behavior, syntax, and rules of each candidate with the request.
5. Select the best component or component combination. Obey all its constraints.
6. Use the exact structure and constraints of the selected components.

You must match the meaning, even when the words are different from component names. A component with a different name can still be the best match. Always examine the intended function and meaning.

If the user requests a named component and a guide with that name exists, read that guide first.
