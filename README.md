# ZERO ユーザーマニュアル

GitHub Pages でホストされるドキュメントサイト。

## ローカル起動

```bash
cd docs
bundle install
bundle exec jekyll serve
```

http://localhost:4000/zero_user_manual/ で確認できる。

**Ruby 3.4.x が必要。** `rbenv global 3.4.8` 等で切り替え。

## 画像の追加

```bash
# スクショをクリップボードにコピーした状態で
paste-img <name>
# → docs/images/<name>.png に保存
# → Markdown参照がクリップボードにコピーされる
```

`paste-img` は `~/dotfiles/bin/paste-img` にある。`brew install pngpaste` が必要。

## ページ構成

| パス | 内容 |
|------|------|
| `docs/index.md` | TOP（一覧） |
| `docs/getting-started.md` | ご利用開始ガイド |
| `docs/manual.md` | 活用ガイド |
| `docs/images/` | 画像 |
| `docs/_layouts/default.html` | レイアウト・CSS・TOC |
