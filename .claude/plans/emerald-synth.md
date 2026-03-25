# Emerald Synth — テーマ開発プラン

## 概要

Maestro の "Dre Synth" テーマにインスパイアされた synthwave 系カラーテーマ。
現在 dotfiles で使用している Cyberdyne ベースのネオングリーン (#00ff92) を軸に、
独立テーマとして設計・公開する。

リポジトリ: `malleroid/emerald-synth`

## 対象ツール (展開順)

1. **Ghostty** (terminal theme) — 最初に着手
2. **Neovim** (colorscheme plugin)
3. **Vivaldi** (browser theme)
4. **Obsidian** (CSS snippet)
5. **Slack** (sidebar theme)

## リポジトリ構成案

```
emerald-synth/
├── palette.toml          # 単一のカラー定義ソース (single source of truth)
├── ghostty/
├── nvim/                 # Neovim プラグインとして独立公開も検討
├── vivaldi/
├── obsidian/
├── slack/
└── scripts/              # palette → 各フォーマット変換
```

## ステップ

### Phase 1: パレット設計
- [ ] Dre Synth のカラー情報を調査
- [ ] ベースパレットを設計 (16色 ANSI + fg/bg/cursor + 拡張色)
- [ ] palette.toml に定義

### Phase 2: Ghostty テーマ
- [ ] Ghostty テーマファイル形式で実装
- [ ] 実際のターミナル上で動作確認・調整
- [ ] Ghostty themes repo への PR も検討

### Phase 3: Neovim colorscheme
- [ ] Lua ベースの colorscheme プラグインとして実装
- [ ] highlight group のカバレッジ (TreeSitter, LSP, 主要プラグイン)
- [ ] パレットから不足色があれば追加
- [ ] `use "malleroid/emerald-synth"` で使える形にする

### Phase 4: その他ツール展開
- [ ] Vivaldi — CSS カスタムテーマ or テーマ設定 JSON
- [ ] Obsidian — CSS snippet
- [ ] Slack — サイドバーテーマ (カラーコード数個)

### Phase 5: 公開・整備
- [ ] README (スクリーンショット付き)
- [ ] インストール手順 (各ツール)
- [ ] dotfiles 側でテーマを参照するように設定変更

## 設計方針

- パレット定義を1箇所 (palette.toml) で管理し、各ツール向けフォーマットを生成する構造
- Neovim 等で不足する色が出たらパレットに追加していく (パレットは成長する前提)
- 現在の Cyberdyne/cyberdream 環境からの移行がスムーズにできるようにする

## 現在の dotfiles での関連設定 (参考)

- Ghostty: `theme = Cyberdyne`, bg opacity 0.75
- Neovim: cyberdream.nvim + カスタムカラーオーバーライド (bg: #151144, fg: #00ff92 等)
- Zellij: custom-nord テーマ (Cyberdyne 補色の magenta #FF0369)
- Fish: 手動カラー設定
- Starship: カスタム hex カラー
