# Notepad++のインストール

MkDocsのMarkdown記法はWindows付属のメモ帳でも可能ですが、
文字コードや改行コードの対応に難があったり、複雑な記述は見づらかったりするため、
編集ツールとしてフリーソフトの `Notepad++` をインストールします。
タブ機能や学習する入力補完機能があります。

## Notepad++ダウンロード

[Notepad++公式サイト](https://notepad-plus-plus.org/download)から `Current Version 7.8.6` → `Download 64-bit x64 Installer` を選択してダウンロードします。
2020年6月時点の最新バージョンは `npp.7.8.6.Installer.x64.exe`です。

## Notepad++セットアップ

![Notepad++ コンポーネントを選んでください](img\np01.png "Notepad++ コンポーネントを選んでください")

|オプション|内容|
|--------|----|
|Localization|Japanese` にチェックするとメニューなどが日本語になります。(後から変更できます)|
|Context Menu Entry|エクスプローラーの右クリックメニューに`Edit with Notepad++` (Notepad++で開く)の項目が追加されます。メニューが増えるのが煩わしい場合はチェックを外します。|
|Create Shortcut on Desktop|デスクトップにショートカットが作成されます。|
|Don't user %APPDATA%|Notepad++の個人設定が通常 `C:\Users\Name\AppData\Roaming\Notepad++` に作成されるのが、インストールフォルダに作成されるようになります。Windowsユーザー環境を汚さず、設定をUSBに入れて持ち運びたい時にチェックします。|

![Notepad++ change.log](img\np03.png "Notepad++ change.log")

Notepad++の `change.log` が表示されればインストール完了です。
