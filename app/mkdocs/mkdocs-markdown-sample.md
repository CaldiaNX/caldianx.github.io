# MkDocsで使えるMarkdownサンプル

ここではMkDocsで使えるマークアップについて解説します。  
Markdown記法がベースになります。

## 見出し

```
# 見出し1
## 見出し2
### 見出し3
#### 見出し4
##### 見出し5
###### 見出し6

見出し1
=============
見出し2
-------------

```

目次が崩れるので表示例は省略。

- 見出し1は各ページの先頭に1つ、見出し2は見出し1より下に書くことで目次が自動作成されます。  
- ページタイトルは短く、見出し1は情報を詰め込むとメニューに改行ができないため見栄えが良くなります。

## 引用

```
> 引用です。  
> 引用です。
>
>> 二重引用です。  
>> 二重引用です。
```

> 引用です。  
> 引用です。
>
>> 二重引用です。  
>> 二重引用です。

## pre記法

```
	#pre表記
		先頭をタブにすることで段落表記が可能。
    #pre表記
        先頭を半角スペース4つにすることで段落表記が可能。
```

	#pre表記
		先頭をタブにすることで段落表記が可能。
    #pre表記
        先頭を半角スペース4つにすることで段落表記が可能。

## code記法

```
バッククォートで文字列を囲むことで`コードの一部`を表示可能です。
```

バッククォートで文字列を囲むことで`コードの一部`を表示可能です。

## 文字修飾

``` md
改行は末尾に半角スペースを2文字入れます。  
*italic* または _斜文字_  
**bold** または __太字__  
***bold*** または ___強調___
```

改行は末尾に半角スペースを2文字入れます。  
*italic* または _斜文字_  
**bold** または __太字__  
***bold*** または ___強調___

## 水平線

``` md
***

アスタリスクを3つ  

---
ハイフンを3つ  
___
アンダースコアを3つ  
************************************************************
* * *
アスタリスク大量またはスペース含む
```

*** 

アスタリスクを3つ  

---
ハイフンを3つ  
___
アンダースコアを3つ  
************************************************************
* * *
アスタリスク大量またはスペース含む

!!! Tip
    意図しないマークアップになる可能性が高いので、水平線を使う場合は上下を空けるほうが良い。

## リンク

`[表示文字](リンクURL "Title属性")`でリンクを記述できます。  
`[定義文字]:URL "Title属性"`で定義参照も出来ます。

``` md
[google](https://www.google.co.jp/ "ぐーぐる")と[yahoo](https://www.yahoo.co.jp/ "やふー")  
[あっちにgoogle][google]（その他の文章）[こっちにyahoo][yahoo]  
URL( https://www.google.co.jp/ )だけではリンクは作成されない。  
サイト内は[mdファイル](index.md)の指定で変換できます。

[google]: https://www.google.co.jp/ "ぐーぐるさん"
[yahoo]: https://www.yahoo.co.jp/ (やふーさん)
```

[google](https://www.google.co.jp/ "ぐーぐる")と[yahoo](https://www.yahoo.co.jp/ "やふー")  
[あっちにgoogle][google]（その他の文章）[こっちにyahoo][yahoo]  
URL( https://www.google.co.jp/ )だけではリンクは作成されない。  
サイト内は[mdファイル](index.md)の指定で変換できます。

[google]: https://www.google.co.jp/ "ぐーぐるさん"
[yahoo]: https://www.yahoo.co.jp/ (やふーさん)

## テーブル

幾つか記載方法があります。文字寄せも可能。
テーブル内の改行は`<br />`タグで改行できます。

```md
First Header | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | 改行は<br />で行う

First Header | Second Header | Third Header
:----------- |:-------------:| -----------:
Left         | Center        | Right
Left         | Center        | Right

| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell |
| Content Cell | Content Cell  | Content Cell |
```

First Header | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | 改行は<br />で行う

First Header | Second Header | Third Header
:----------- |:-------------:| -----------:
Left         | Center        | Right
Left         | Center        | Right

| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell |
| Content Cell | Content Cell  | Content Cell |

## リスト

リスト上下に空白が必要です。

```md
*   Red
*   Green
    *   Blue
---
+   Red
+   Green
    +   Blue
---
-   Red
-   Green
    -   Blue
---
1.  Bird
1.  McHale
    1.  Parish
```

*   Red
*   Green
    *   Blue
---
+   Red
+   Green
    +   Blue
---
-   Red
-   Green
    -   Blue
---
1.  Bird
1.  McHale
    1.  Parish

## 画像

`![alt文字列](画像URL “title文字列”)`で画像が表示されます。  
ハイパーリンクと同じように外部参照も利用できます。

```
![赤](img\sample_red.png "赤色")

![青][blue]
[blue]:img\sample_blue.png "青色"

[![緑](img\sample_green.png "緑色ファイルにリンク")](img\sample_green.png)

[![黄](img\sample_yellow.png "黄色ファイルにリンク")][yellow]
[yellow]: img\sample_yellow.png "黄色"
```

![赤](img\sample_red.png "赤色") ![青][blue] [![緑](img\sample_green.png "緑色ファイルにリンク")](img\sample_green.png) [![黄](img\sample_yellow.png "黄色ファイルにリンク")][yellow]
[blue]:img\sample_blue.png "青色"
[yellow]: img\sample_yellow.png "黄色"

## エスケープ

`￥(バックスラッシュ)` でマークアップをエスケープできます。

```
\ # タイトル
```

\ # タイトル

## コメントアウト

HTMLタグの`<!-- -->` を使ってコメントアウトします。

```
<!-- コメントアウトを書きます -->
```

<!-- コメントアウトを書きます -->


## 参考リンク
- [MkDocsによるドキュメント作成 - Qiita](https://qiita.com/mebiusbox2/items/a61d42878266af969e3c)
- [MkDocs で生成したサイトをローカルで開くと index.html が開かれない問題 - stamemo](http://stakiran.hatenablog.com/entry/2018/08/02/202958)
- [MkDocs Themes ・ mkdocs/mkdocs Wiki ・ GitHub](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes)
- [Icons - Material Design](https://material.io/resources/icons/?style=baseline)
- [The Web App Manifest ?|? Web Fundamentals ?|? Google Developers](https://developers.google.com/web/fundamentals/web-app-manifest/?hl=ja)
- [MkDocsでドキュメント管理 - notebook](https://swfz.hatenablog.com/entry/2015/07/28/031712)
- [Markdown記法まとめ(リスト、リンク、画像、インラインHTML、エスケープ)[2/3] - はしくれエンジニアもどきのメモ](https://cartman0.hatenablog.com/entry/2015/03/31/164836)
