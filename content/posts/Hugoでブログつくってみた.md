---
title: "Hugoでブログつくってみた"
date: 2021-05-16T22:34:33+09:00
draft: false
---

お試しで作ってみたのでテスト
以下メモ
# 環境構築
```sh
brew install hugo
hugo new site blog-name

cd blog-name
git init
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
echo 'theme = "ananke"' >> config.toml
```

# 記事作成
```sh
hugo new posts/pos-namet.md # 記事作成
hugo server -D # ドラフト含めてローカルで確認
```

# Netlify設定
netlify.tomlを作成してリポジトリにpush
```toml:netlify.toml
[build]
publish = "public"
command = "hugo --theme=ananke --gc --minify"
[build.environment]
HUGO_VERSION = "0.83.0"
```

# 参考
https://blog.u-chan-chi.com/post/hugo/
https://qiita.com/jrfk/items/4c6df87ca72a76e30224

