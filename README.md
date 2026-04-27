# One Dark Pro for Nimbalyst

Atom's iconic One Dark theme for Nimbalyst, ported from the
[Binaryify/OneDark-Pro](https://github.com/Binaryify/OneDark-Pro) VS Code theme.

Ships two variants:

- **One Dark Pro** — the classic `#282c34` background
- **One Dark Pro Darker** — `#1b1f23` background for higher contrast

## Install in Nimbalyst

This extension contains only a theme contribution, so there's no build step —
the prebuilt `dist/index.js` is just an empty lifecycle stub.

1. Enable **Settings > Advanced > Extension Dev Tools** in Nimbalyst.
2. Ask Claude inside Nimbalyst:

   > Install my extension from `~/sites/Nola/nimbalyst-onedark-pro`

   Claude calls the `extension_install` tool to register it.
3. Open the theme picker and select **One Dark Pro** or **One Dark Pro Darker**.

While iterating on `manifest.json`, ask Claude to **reload** the extension and
the new colors will apply live.

## What's covered

The manifest maps the One Dark Pro palette to every Nimbalyst theme token —
backgrounds, text, borders, status colors, code blocks, syntax highlighting
(`code-comment`, `code-property`, `code-function`…), diff add/remove, scrollbar,
terminal foreground/background, cursor, and the full 16-color ANSI palette.

Tokens you don't override are inherited from Nimbalyst's built-in dark theme,
and a few are auto-derived (e.g. `terminal-bg` falls back to `bg-secondary`).

## Files

```
nimbalyst-onedark-pro/
  manifest.json     # both theme variants live here
  package.json      # metadata only
  dist/index.js     # empty activate/deactivate stub
  README.md
```

## Credits

- Original VS Code theme: [Binaryify/OneDark-Pro](https://github.com/Binaryify/OneDark-Pro)
  (MIT)
- Inspired by the One Dark UI from [Atom](https://github.com/atom/atom)
