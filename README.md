# Emerald Synth

A synthwave-inspired dark color theme with deep purple backgrounds and cyan-green accents.

## Palette

| Role | Color | Hex |
|------|-------|-----|
| Background | ![#0d0221](https://placehold.co/16x16/0d0221/0d0221) | `#0d0221` |
| Foreground | ![#f0e6ff](https://placehold.co/16x16/f0e6ff/f0e6ff) | `#f0e6ff` |
| Accent | ![#00ffcc](https://placehold.co/16x16/00ffcc/00ffcc) | `#00ffcc` |
| Border | ![#00d4aa](https://placehold.co/16x16/00d4aa/00d4aa) | `#00d4aa` |
| Warning / Error | ![#ff2a6d](https://placehold.co/16x16/ff2a6d/ff2a6d) | `#ff2a6d` |

Full palette definition: [`palette.toml`](palette.toml)

## Supported Tools

### Ghostty

Terminal theme with ANSI 16 colors, cursor/selection, search highlighting, and split-divider.

**Install:**
```sh
ln -s /path/to/emerald-synth/ghostty/emerald-synth ~/.config/ghostty/themes/emerald-synth
```
Then add `theme = emerald-synth` to `~/.config/ghostty/config`.

### Zellij

Terminal multiplexer theme (KDL format, new component-based spec).

**Install:**
```sh
cp zellij/emerald-synth.kdl ~/.config/zellij/themes/
```
Then add `theme "emerald-synth"` to `~/.config/zellij/config.kdl`.

### Zed

Editor theme with full UI styling, syntax highlighting, and terminal ANSI colors (normal/bright/dim).

**Install:**
```sh
ln -s /path/to/emerald-synth/zed/emerald-synth.json ~/.config/zed/themes/emerald-synth.json
```
Then select "Emerald Synth" in Zed: `Cmd+K Cmd+T`.

### Vivaldi

Browser theme with radial glow background. See [`vivaldi/README.md`](vivaldi/README.md) for details.

**Install:** Settings > Themes > Import theme (zip `vivaldi/theme/settings.json` + `vivaldi/theme/background.png`)

### Slack

Custom theme colors. See [`slack/theme.txt`](slack/theme.txt).

**Install:** Settings > Appearance > Custom theme

### Obsidian

Community theme with Foundation base colors, semantic styling, heading gradient, syntax highlighting, callouts, and graph colors.

**Install:**
```sh
# Symlink into vault
mkdir -p /path/to/vault/.obsidian/themes/Emerald\ Synth
ln -s /path/to/emerald-synth/obsidian/theme.css /path/to/vault/.obsidian/themes/Emerald\ Synth/theme.css
ln -s /path/to/emerald-synth/obsidian/manifest.json /path/to/vault/.obsidian/themes/Emerald\ Synth/manifest.json
```
Then select "Emerald Synth" in Obsidian: Settings > Appearance > Themes.

### Neovim

Lua colorscheme with editor UI, syntax, TreeSitter, LSP diagnostics, and plugin integrations (Telescope, Gitsigns).

**Install (lazy.nvim):**
```lua
{
  "malleroid/emerald-synth.nvim",
  lazy = false,
  priority = 1000,
  config = function()
    require("emerald-synth").setup({})
    vim.cmd.colorscheme("emerald-synth")
  end,
}
```

**Install (local dev):**
```sh
nvim --cmd "set rtp^=/path/to/emerald-synth/nvim" -c "colorscheme emerald-synth"
```

## License

[MIT](LICENSE)
