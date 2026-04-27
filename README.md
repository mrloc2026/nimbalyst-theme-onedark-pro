# One Dark Pro for Nimbalyst

Atom's iconic One Dark theme, ported from
[Binaryify/OneDark-Pro](https://github.com/Binaryify/OneDark-Pro) for the
Nimbalyst editor (v0.58.x).

Two variants:

- **One Dark Pro** — the classic `#282c34` background
- **One Dark Pro Darker** — `#1b1f23` for higher contrast

## Layout

```
nimbalyst-onedark-pro/
├── onedark-pro/
│   └── theme.json
└── onedark-pro-darker/
    └── theme.json
```

Each subfolder is a standalone Nimbalyst theme bundle. `theme.json` follows
Nimbalyst's filesystem theme schema (id, name, version, isDark, colors, tags).

## Install (manual)

The Themes panel in Settings reads themes from
`~/Library/Application Support/@nimbalyst/electron/themes/` (macOS).
Until Nimbalyst ships an Install button, copy the bundles in directly:

```bash
git clone https://github.com/mrloc2026/nimbalyst-theme-onedark-pro.git
cd nimbalyst-theme-onedark-pro

# macOS
DEST="$HOME/Library/Application Support/@nimbalyst/electron/themes"
mkdir -p "$DEST"
cp -R onedark-pro "$DEST/"
cp -R onedark-pro-darker "$DEST/"
```

Then in Nimbalyst:

1. Open **Settings → Themes**
2. Click **Refresh** (top-right)
3. **One Dark Pro** and **One Dark Pro Darker** appear under *Installed Themes*
4. Click **Apply** on either

## Why not an extension?

Nimbalyst's older extension `contributions.themes` schema isn't wired up to the
Themes panel in v0.58.x. Themes have to be filesystem bundles in the user
themes dir to show up. If you previously installed this as a Marketplace
extension, you can uninstall it from **Settings → Marketplace → Installed**.

## Color schema

Nimbalyst v0.58.x's `ThemeLoader` accepts these 20 keys; anything else is
warned and ignored:

```
bg, bg-secondary, bg-tertiary, bg-hover, bg-selected, bg-active,
text, text-muted, text-faint, text-disabled,
border, border-focus,
primary, primary-hover,
link, link-hover,
success, warning, error, info
```

## Credits

- Original VS Code theme: [Binaryify/OneDark-Pro](https://github.com/Binaryify/OneDark-Pro)
  (MIT)
- Inspired by the One Dark UI from [Atom](https://github.com/atom/atom)
