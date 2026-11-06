# daisyUI 4 skill

[![skills.sh](https://skills.sh/b/arvin0494/daisyui-4)](https://skills.sh/arvin0494/daisyui-4)

An agent skill for **daisyUI 4 + Tailwind CSS 3**, written for projects that must run on older browsers — including **Firefox 115 ESR on Windows 7**.

daisyUI 5 and Tailwind CSS 4 require Firefox 128+, so they cannot be used when Firefox 115 ESR has to keep working. This skill covers the v4 API instead: `tailwind.config.js`, `@apply`, `join-item`, `!bg-red-500`, and the rest of the v4 class set.

> Unofficial. Not affiliated with daisyUI. See [Credits](#credits).

## Install

With the [skills CLI](https://www.skills.sh/docs/cli):

```sh
npx skills add arvin0494/daisyui-4
```

Install globally for a specific agent without prompts:

```sh
npx skills add arvin0494/daisyui-4 -g -a opencode -y
```

Manual install for OpenCode:

```sh
git clone https://github.com/arvin0494/daisyui-4 /tmp/daisyui-4
cp -r /tmp/daisyui-4/skills/daisyui-4 ~/.config/opencode/skills/
```

Use `~/.agents/skills/`, `.opencode/skills/`, or `.claude/skills/` instead if that is where your agent looks. The folder must contain `SKILL.md` at its root.

## Use

The agent picks the skill up when the project uses daisyUI 4. To force it, mention `@daisyui-4`.

`SKILL.md` is the entry point and routes to these guides:

| Guide | Contents |
| --- | --- |
| `install/SKILL.md` | npm, `tailwind.config.js`, CDN, framework installs |
| `usage/SKILL.md` | Class-name rules, `@apply`, utilities |
| `config/SKILL.md` | Themes, prefix, logs, `themeRoot` |
| `colors/SKILL.md` | Semantic colors and custom themes |
| `components/*.md` | 55 components, one file each |

## Why v4

| | daisyUI 4 + Tailwind 3 | daisyUI 5 + Tailwind 4 |
| --- | --- | --- |
| Firefox | 115 ESR and newer | 128+ |
| Tailwind config | `tailwind.config.js` | CSS `@plugin` |
| Component overrides | `@apply` | `@utility` |
| Components | 55 | 68 |
| CDN | `dist/full.min.css` + `cdn.tailwindcss.com` | `daisyui@5` + `@tailwindcss/browser` |

## Contents

```
skills/daisyui-4/
├── SKILL.md
├── install/SKILL.md
├── usage/SKILL.md
├── config/SKILL.md
├── colors/SKILL.md
└── components/*.md
```

55 component guides, including `artboard` and `bottom-navigation`, which were removed in daisyUI 5.

## Compatibility notes

The skill tells the agent to avoid features that Firefox 115 ESR does not support:

| Feature | Minimum Firefox | Note |
| --- | --- | --- |
| `:has()` | 121 | Only `theme-controller` uses it; use `data-theme` + JavaScript |
| CSS nesting | 117 | Write flat selectors |
| `text-wrap: balance` | 121 | Do not use `text-balance` |
| `light-dark()` | 120 | Not supported |
| `@property` | 128 | Not supported |
| Relative color syntax | 128 | Not supported |
| `color-mix()`, `oklch()` | 113 | Safe |

## Accuracy

Class names are checked against the shipped `daisyui@4.12.24/dist/full.css`. CDN URLs in the install guide return the expected content types:

- `https://cdn.jsdelivr.net/npm/daisyui@4.12.24/dist/full.min.css` → `text/css`
- `https://cdn.tailwindcss.com` → `text/javascript`
- `https://cdn.jsdelivr.net/npm/daisyui@4.12.24/dist/themes.css` → `text/css`

## Credits

- [daisyUI](https://daisyui.com) © Pouya Saadeghi, MIT License.
- The structure follows the official daisyUI 5 skill at <https://daisyui.com/SKILL.md>.
- This v4 port is unofficial and maintained separately.

## Contributing

Issues and pull requests are welcome. If you add or change a class name, verify it against `daisyui@4.12.24/dist/full.css` first.

## License

MIT — see [LICENSE](LICENSE).
