# Utility Classes to CSS

Paste a string of Tailwind utility classes and get the equivalent plain CSS, grouped into a single rule. It covers a solid set of common utilities using the default theme values. It is honest about scope: this maps common utilities with the default theme, not every plugin, variant, or custom config.

**Live demo:** https://0xelitesystem.github.io/utility-classes-to-css/

## Use

1. Paste Tailwind classes into the input, or click Load sample.
2. Click Convert, or press Ctrl or Cmd plus Enter.
3. Read the generated CSS rule and the list of classes it did not recognize, then click Copy.

## Why this exists

Sometimes you need the plain CSS behind a set of Tailwind classes: for an email template, for a project without Tailwind, or to learn what a class actually does. This tool maps common utilities in one HTML file with no build, no tracking, and no network calls, released under the MIT license.

## Features

- Maps spacing (margin and padding with sides and the standard scale), sizing (width and height), typography (size, weight, align, and basic color), colors (background and text using the default palette values), flex and grid basics, gap, rounded, border, shadow, display, and position.
- Groups every recognized declaration into a single CSS rule.
- Notes any classes it did not recognize so you can spot gaps.
- Copy button for the generated CSS.
- Dark mode toggle, keyboard friendly (Ctrl or Cmd plus Enter to convert).
- One file, no external dependencies, works offline.

## How it works

Each class in your input is parsed and matched against a lookup of common Tailwind utilities and the default theme scale (spacing, palette shades 50 to 950, font sizes, radii, and shadows). Matched declarations are merged, with later classes overriding earlier ones for the same property, then printed as a single `.converted` rule. Variant prefixes such as `hover:` or `md:` cannot be represented in a flat rule, so the base class is mapped and the variant is flagged. Unrecognized classes are listed separately.

## Privacy

Everything runs in your browser. Your input, the parsing, and the output never leave your machine. There are no external requests, no analytics, and no tracking. Open the page source or the network tab to confirm.

If you use the theme toggle, your light or dark choice is saved in your browser's localStorage under the key `theme`. Nothing else is stored.

## Run locally

```
git clone https://github.com/0xelitesystem/utility-classes-to-css
cd utility-classes-to-css
```

Open `index.html` in a browser, or serve the folder with `python -m http.server` and visit http://localhost:8000.

## Build

No build step. The whole tool is one `index.html` file.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright RBL Industries LLC 2026.
