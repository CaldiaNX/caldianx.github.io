# MkDocsのインストール

## MkDocsのインストール

コマンドプロンプトから `py -m pip install mkdocs` を実行します。
環境変数PATHにPythonを登録せず、Pythonランチャー（`py.exe`）を利用している場合、コマンドプロンプトからの実行は `py -m` を付けます。

``` bat
py -m pip install mkdocs
Collecting mkdocs
  Downloading mkdocs-1.1.2-py3-none-any.whl (6.4 MB)
     |████████████████████████████████| 6.4 MB 3.3 MB/s
Collecting Markdown>=3.2.1
  Downloading Markdown-3.2.2-py3-none-any.whl (88 kB)
     |████████████████████████████████| 88 kB ...
Collecting PyYAML>=3.10
  Downloading PyYAML-5.3.1-cp38-cp38-win32.whl (199 kB)
     |████████████████████████████████| 199 kB ...
Collecting Jinja2>=2.10.1
  Downloading Jinja2-2.11.2-py2.py3-none-any.whl (125 kB)
     |████████████████████████████████| 125 kB 6.8 MB/s
Collecting click>=3.3
  Downloading click-7.1.2-py2.py3-none-any.whl (82 kB)
     |████████████████████████████████| 82 kB ...
Collecting lunr[languages]==0.5.8
  Downloading lunr-0.5.8-py2.py3-none-any.whl (2.3 MB)
     |████████████████████████████████| 2.3 MB ...
Collecting livereload>=2.5.1
  Using cached livereload-2.6.1-py2.py3-none-any.whl (23 kB)
Collecting tornado>=5.0
  Downloading tornado-6.0.4-cp38-cp38-win32.whl (416 kB)
     |████████████████████████████████| 416 kB 6.8 MB/s
Collecting MarkupSafe>=0.23
  Downloading MarkupSafe-1.1.1-cp38-cp38-win32.whl (16 kB)
Collecting six>=1.11.0
  Downloading six-1.15.0-py2.py3-none-any.whl (10 kB)
Collecting future>=0.16.0
  Using cached future-0.18.2.tar.gz (829 kB)
Collecting nltk>=3.2.5; python_version > "2.7" and extra == "languages"
  Downloading nltk-3.5.zip (1.4 MB)
     |████████████████████████████████| 1.4 MB 6.8 MB/s
Collecting joblib
  Downloading joblib-0.15.1-py3-none-any.whl (298 kB)
     |████████████████████████████████| 298 kB ...
Collecting regex
  Downloading regex-2020.5.14-cp38-cp38-win32.whl (251 kB)
     |████████████████████████████████| 251 kB ...
Collecting tqdm
  Downloading tqdm-4.46.1-py2.py3-none-any.whl (63 kB)
     |████████████████████████████████| 63 kB 4.5 MB/s
Installing collected packages: Markdown, PyYAML, MarkupSafe, Jinja2, click, six, future, joblib, regex, tqdm, nltk, lunr, tornado, livereload, mkdocs
  WARNING: The script markdown_py.exe is installed in 'C:\Python\Python38-32\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
    Running setup.py install for future ... done
  WARNING: The script tqdm.exe is installed in 'C:\Python\Python38-32\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
    Running setup.py install for nltk ... done
  WARNING: The script livereload.exe is installed in 'C:\Python\Python38-32\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  WARNING: The script mkdocs.exe is installed in 'C:\Python\Python38-32\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed Jinja2-2.11.2 Markdown-3.2.2 MarkupSafe-1.1.1 PyYAML-5.3.1 click-7.1.2 future-0.18.2 joblib-0.15.1 livereload-2.6.1 lunr-0.5.8 mkdocs-1.1.2 nltk-3.5 regex-2020.5.14 six-1.15.0 tornado-6.0.4 tqdm-4.46.1
WARNING: You are using pip version 20.0.2; however, version 20.1.1 is available.
You should consider upgrading via the 'C:\Python\Python38-32\python.exe -m pip install --upgrade pip' command.
```

バージョンを確認します。

``` bat
C:\Users\NAME>py -m mkdocs -V
__main__.py, version 1.1.2 from C:\Python\Python38-32\lib\site-packages\mkdocs (Python 3.8)
```

バージョンが表示されればインストール完了です。

## プロジェクトの新規作成

Pythonフォルダ直下に例として `MkDocsSample` プロジェクトを新規作成します。
プロジェクトフォルダが作成されて、中に `mkdocs.yml` ファイルと `docs` フォルダが作成されます。
`docs` フォルダには `index.md` ファイルが作成されます。

``` bat
C:\Users\NAME>cd C:\python
C:\python>py -m mkdocs new MkDocsSample
INFO    -  Creating project directory: MkDocsSample
INFO    -  Writing config file: MkDocsSample\mkdocs.yml
INFO    -  Writing initial docs: MkDocsSample\docs\index.md
```

index.mdはMarkdown形式のテキストファイルです。

![MkDocs index.md](img\mkdocs01.png "MkDocs index.md")

## プロジェクトのビルド

プロジェクトをビルドするにはプロジェクトフォルダに `cd` で移動し、 `mkdocs build` コマンドでビルドします。
ビルドが成功すれば新規作成された `site` フォルダにファイル一式が出力されます。

``` bat
C:\Python>cd MkDocsSample
C:\Python\MkDocsSample>py -m mkdocs build
INFO    -  Cleaning site directory
INFO    -  Building documentation to directory: C:\Python\MkDocsSample\site
INFO    -  Documentation built in 0.22 seconds
```

![MkDocs index.html ブラウザ表示](img\mkdocs02.png "MkDocs indexl.html ブラウザ表示")

mdファイルの修正や作成とbuildを繰り返して作業します。

## ローカルサーバーの起動

HTMLファイルのサイト内リンクはディレクトリパスを参照するため、リンク移動すると下記のようなディレクトリ画面が表示されてしまうため、サイト内の移動がやや面倒です。

![MkDocs ディレクトリ表示](img\mkdocs03s.png "MkDocs ディレクトリ表示")

`mkdocs serve` コマンドを使うとローカルでHTTPサーバサービスが起動します。
アドレスが表示される（下記では [http://127.0.0.1:8000](http://127.0.0.1:8000) ）のでWebブラウザで表示します。  
HTTPサーバサービスでは本来の挙動(サイト内リンクでindex.htmlが表示など)になります。  
また、サービス起動中はファイルの変更が自動的に反映されるため毎回ビルドしなくて済みます。

``` bat
C:\Python\MkDocsSample>mkdocs serve
INFO    -  Building documentation...
INFO    -  Cleaning site directory
[I 190901 12:34:56 server:296] Serving on http://127.0.0.1:8000
[I 190901 12:34:56 handlers:62] Start watching changes
[I 190901 12:34:56 handlers:64] Start detecting changes
```

終了させる場合はコマンドプロンプトを閉じるか、 ++ctrl+c++ を押します。

``` bat
[I 190901 12:35:00 server:318] Shutting down...
```

## 文字コードについて

MkDocsのファイルはUTF-8で作成します。  
Windows標準のメモ帳でテキストが空、もしくは**半角英数字で書かれたファイルに全角文字を追加して保存**した場合、**Shift_JIS**で保存されてしまうことがあります。
この状態でビルドすると**UnicodeDecodeError**となってしまいます。
その場合は保存時に文字コードをUTF-8に変更して上書き保存してください。

``` bat
C:\Python\MkDocsSample>mkdocs build
INFO    -  Cleaning site directory
INFO    -  Building documentation to directory: C:\Python\MkDocsSample\site
ERROR   -  Encoding error reading file: index.md
ERROR   -  Error reading page 'index.md': 'utf-8' codec can't decode byte 0x82 in position 8: invalid start byte
（省略）
UnicodeDecodeError: 'utf-8' codec can't decode byte 0x82 in position 8: invalid start byte
```
