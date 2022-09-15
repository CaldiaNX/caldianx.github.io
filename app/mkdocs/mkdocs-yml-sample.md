# mkdocs.ymlのサンプル

MkDocsプロジェクトフォルダの `mkdocs.yml` ファイルを編集することでサイト情報のカスタマイズやプラグインの導入が可能です。
下記のサンプルでは本ドキュメントの `mkdocs.yml` を編集して掲載しています。

``` yaml
# サイト名。ヘッダーに記載
site_name: 'Caldia MkDocs Manual'
# metaのdescription属性。検索サイトの表示用文章
site_description: 'MkDocsの導入手順を解説。'
# metaのauthor属性。サイト管理者名
site_author: 'Caldia'
# metaのcanonical属性。HTMLを表示するサイトのトップページURL
site_url: 'https://caldia.tuzikaze.com/'
# Copyright。HTMLのフッター。無くても良い。書式も特に決まりはない
copyright: 'Copyright (c) 2006 - 2022 Caldia All rights reserved.'
# サイトの構成。（旧版のpages）
# ページを追加する場合はここにページ名とファイル名を記載
nav:
    - 'はじめに': index.md
    - 'Pythonのインストール': install-python.md
    - 'MkDocsのインストール': install-mkdocs.md
    - 'Markdownのサンプル': markdown-sample.md
    - 'ymlファイルのサンプル': mkdocs-yml-sample.md
    - 'Materialテーマの導入': install-mkdocs-material.md
    # URL直接指定
    - 'link:トップに戻る' : https://caldia.tuzikaze.com/studio
    - 'link:CaldiaのVRM Room' : https://caldia.tuzikaze.com
    # 子ページの作成も可能
    - Test:
        - page1: test/page1.md
        - page2: test/page2.md

# カスタマイズしたCSSファイルを読み込む
extra_css: [style.css]

```

## mkdocs.yml出力例

上記の `mkdocs.yml` をビルドしたHTMLのヘッダーは以下のように生成されます。

``` html
<!doctype html>
<html lang="ja" class="no-js">
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width,initial-scale=1">
        <meta http-equiv="x-ua-compatible" content="ie=edge">
        <meta name="description" content="MkDocsの導入手順を解説。 ">
        <link rel="canonical" href="https://caldia.tuzikaze.com/mkdocs/">
        <meta name="author" content="Caldia">
        <link rel="shortcut icon" href="assets/images/favicon.png">
        <meta name="generator" content="mkdocs-1.0.4, mkdocs-material-4.4.2">
        <title>Caldia MkDocs Manual</title>
		<link rel="stylesheet" href="../style.css">
    </head>
・・・
```