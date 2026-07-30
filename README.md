# Tailwind to CSS

Paste a string of Tailwind utility classes and get the equivalent plain CSS, grouped into a single rule. It covers a solid set of common utilities using the default theme values. It is honest about scope: this maps common utilities with the default theme, not every plugin, variant, or custom config.

## Live demo

https://0xelitesystem.github.io/tailwind-to-css/

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

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.
