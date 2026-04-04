# Emerald Synth for Zellij

A synthwave-inspired dark theme for [Zellij](https://zellij.dev) with deep purple backgrounds and emerald-green foreground text.

## Preview

| Role | Color | Hex |
|------|-------|-----|
| Text base | ![#00ffcc](https://placehold.co/16x16/00ffcc/00ffcc) | `#00ffcc` |
| Ribbon selected | ![#ff79c6](https://placehold.co/16x16/ff79c6/ff79c6) | `#ff79c6` |
| Ribbon unselected | ![#00ffcc](https://placehold.co/16x16/00ffcc/00ffcc) | `#00ffcc` |
| Frame selected | ![#ff79c6](https://placehold.co/16x16/ff79c6/ff79c6) | `#ff79c6` |
| Frame unselected | ![#6a5585](https://placehold.co/16x16/6a5585/6a5585) | `#6a5585` |
| Success | ![#00ffcc](https://placehold.co/16x16/00ffcc/00ffcc) | `#00ffcc` |
| Error | ![#ff2a6d](https://placehold.co/16x16/ff2a6d/ff2a6d) | `#ff2a6d` |

## Install

```sh
mkdir -p ~/.config/zellij/themes
cp zellij/emerald-synth.kdl ~/.config/zellij/themes/
```

Then add to `~/.config/zellij/config.kdl`:

```kdl
theme "emerald-synth"
```
