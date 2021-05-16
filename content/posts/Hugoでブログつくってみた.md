---
title: "Hugoでブログつくってみた"
date: 2021-05-16T22:34:33+09:00
draft: false
---

お試しで作ってみたのでテスト

# 基本コマンド
```sh
hugo new posts/pos-namet.md # 記事作成
hugo server -D # ドラフト含めて
```

# テーマ変更
```sh
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke`
```
した後にconfig.tomlに`theme = "ananke"`設定

# Netlify公開
```toml:netlify.toml
[build]
publish = "public"
command = "hugo --theme=ananke --gc --minify"
```

# 参考
https://blog.u-chan-chi.com/post/hugo/