# Pythonのインストール

MkDocsをビルドする環境としてWindowsにPythonをインストールします。
PythonはWindows向けの開発用オールインワンパッケージとして[Anaconda](https://www.anaconda.com/distribution/) などがありますが、
今回はコマンドラインから使用するのでビルド環境のみをインストールします。

## Pythonダウンロード

[Python公式サイト](https://www.python.org/downloads/) から `Download Python` を選択してインストーラーをダウンロードします。
2020年6月時点の最新バージョンは `Python 3.8.3` です。
トップページからダウンロードする場合は32bit版が選択されます。
64bit版が必要な場合は [Python Releases for Windows](https://www.python.org/downloads/windows/) から `Windows x86-64 executable installer` を選択します。  
32bit版と64bit版のどちらを選択するかは利用するライブラリやコンポーネントのバージョンや4GB以上のメモリを利用するか等で判断します。  
特に気にしなければ今回は32bit版を選択します。

## Pythonセットアップ

インストールフォルダなどの設定をしたい場合は `Customize Installation` を選択します。

!["Install Python Setup"](img\py02.png "Pythonセットアップ画面")

|オプション|内容|
|--------|----|
| Install launcher for all users | 全ユーザーがPythonを利用できます。単一ユーザーや、ユーザーごとにPython環境を分ける場合はチェックしません。（管理者権限が必要）|
| Add Python 3.8 to PATH | Windowsの環境変数にPython実行環境のパスを通します。コマンドプロンプトからPythonを実行したい場合はチェック、環境変数を汚したくない場合はチェック不要。後述のPythonランチャーを利用する場合は不要です。 |

## Customize Installation の場合

!["Python Optional Features"](img\py03.png "Pythonオプション機能選択画面")

|オプション|内容|
|--------|----|
| Documentation | Pythonのドキュメンテーションをインストール |
| pip | パッケージ管理機能のpipをインストール |
| tcl/tk and IDLE | GUIツールキットの「Tkinter」と対話モードの開発環境「IDLE」をインストール |
| Python test suite | テストスイートに利用する標準ライブラリをインストール |
| py launcher | Pythonランチャー( `py.exe` )を有効にします。PythonランチャーはPythonバージョンを自動管理するため、環境変数PATHが不要になります。 |
| for all users | 前画面の `Install launcher for all users` と同じ。 |

!["Python Advanced Features"](img\py04.png "Python拡張オプション画面")

|オプション|内容|
|--------|----|
| Install for all users | 前画面の `Install launcher for all users` と同じ。 |
| Associate files with Python | `.py` 拡張子ファイルをPythonランチャーに関連付けします。 .pyファイルをダブルクリックした時に実行するのではなくエディターで起動したい場合はチェックしません。 |
| Create Shortcuts for installed applications | スタートメニューにPythonのショートカットを追加。|
| Add python to environment variables | 前画面の `Add Python 3.8 to PATH` と同じ。|
| Precompile standard library | 標準ライブラリがプリコンパイルされた状態になります。チェックがなくてもライブラリ実行時にコンパイルされるため、初回実行時の僅かな時間短縮以外に影響はありません。|
| Download debugging symbols | VisualStudio等で検出可能なデバッグシンボルをダウンロードします。細かなデバッグをしない場合は不要。 |
| Download debug binarys | VisualStudio等で利用可能なデバッグ用のバイナリファイルをダウンロードします。細かなデバッグをしない場合は不要。 |
| Customize install location | Pythonのインストールパスを設定します。 `C:\Python\Python38-32` などバージョンを表記した短いパス名を推奨。 |

## Pythonバージョン確認

コマンドプロンプトを起動して `py -V` と入力します。  
Pythonの文字とバージョンが表示されれば成功です。

``` cmd
C:\Users\NAME>py -V
Python 3.8.3
```
