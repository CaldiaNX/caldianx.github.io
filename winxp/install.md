# WindowsXPのインストール

このページでは`WindowsXP Professional SP3`のOSインストールについて解説します。

OSのディスクを入れると  
`Setup is inspecting your computer's hardware configration...`  
と表示されるのでしばらく待ちます。

![img](img/windows_xp_install001.png "img")

SCSIやRAIDドライバーを読み込ませたい場合は下記画面で `F6` を押します。  
IDEやAHCIを利用する場合は何もせずに待ちます。

![img](img/windows_xp_install002.png "img")

WindowsXPの新規インストールは［Enter］を押します。

![img](img/windows_xp_install003.png "img")

［F8］を押します。

![img](img/windows_xp_install004.png "img")
 
［半角/全角］キーを押します。

![img](img/windows_xp_install005.png "img")
 
［Y］を押します。

![img](img/windows_xp_install006.png "img")
 
パーティションを複数作成するかどうかを選択します。  
［C］を押してパーティションを作成するとD：やＥ：が作成できます。  
「未使用領域」をそのまま選択するとC：ドライブのみ作成されます。

![img](img/windows_xp_install007.png "img")
 
初回フォーマット方法を選択します。
通常は「NTFSファイルシステムを使用してパーティションをフォーマット（クイック）」を選択します。（通常フォーマットは数時間以上掛かるため注意してください）

![img](img/windows_xp_install008.png "img")

フォーマットが開始されるのでしばらく待ちます。
 
![img](img/windows_xp_install009.png "img")

ディスク検査が始まります。

![img](img/windows_xp_install010.png "img")

ドライブにOSファイルがコピーされます。

![img](img/windows_xp_install011.png "img")

ドライバーのインストールが行われます。

![img](img/windows_xp_install012.png "img")

コンピュータの再起動を促されます。
15秒間そのままにするか、［Enter］を押すと再起動します。

![img](img/windows_xp_install013.png "img")

WindowsXPのロゴが表示されます。
この画面が表示されずに最初の黒画面が表示される場合、コンピュータのドライブ読み込み順がディスク優先に設定されています。
その場合はBIOSで読み込み順をドライブ優先に再設定してください。

![img](img/windows_xp_install014.png "img")

しばらく自動で進みます。

![img](img/windows_xp_install015.png "img")
![img](img/windows_xp_install016.png "img")
![img](img/windows_xp_install017.png "img")
![img](img/windows_xp_install018.png "img")

「次へ」を押します。

![img](img/windows_xp_install019.png "img")

ユーザー名を入力します。組織名は空欄でOKです。
 
![img](img/windows_xp_install020.png "img")

「次へ」を押してスキップします。  
この後の設定でハードウェア構成が大きく変更されたり、OSを再インストールする事態になった場合に再アクティベーションが必要になってしまうため、
プロダクトキーの入力はOSやドライバーのインストールが一段落した段階で入力します。
 
![img](img/windows_xp_install021.png "img")

「いいえ」を押します。

![img](img/windows_xp_install022.png "img")

コンピューター名とAdministratorのパスワードを入力します。
 
![img](img/windows_xp_install023.png "img")

「次へ」を押します。
 
![img](img/windows_xp_install024.png "img")

しばらく自動で進みます。

![img](img/windows_xp_install025.png "img")
![img](img/windows_xp_install026.png "img")
![img](img/windows_xp_install027.png "img")
![img](img/windows_xp_install028.png "img")
![img](img/windows_xp_install029.png "img")
![img](img/windows_xp_install030.png "img")

OKを押します。

![img](img/windows_xp_install031.png "img")
 
解像度が変更されるのでダイアログが見えれば「OK」を押します。
この時点ではグラフィックドライバーが登録されていないので、最適な解像度ではありません。
 
![img](img/windows_xp_install032.png "img")

右下の「次へ」を押します。
 
![img](img/windows_xp_install033.png "img")

「後で設定します」を選択します。
最初のWindowsUpdateは手動で行うためです。
自動を選択すると手動アップデートが自動アップデートと競合して上手くできない場合があります。
また、2014年4月9日以降はWindowsXPのサポート期限が切れているため自動アップデートは出来ません。
 
![img](img/windows_xp_install034.png "img")

ユーザー名を設定します。
日本語名も利用可能ですが、一部プログラムが正しく動かないなどの情報もあるため、英数字を推奨します。
パスワードは後ほど設定します。
 
![img](img/windows_xp_install035.png "img")

「次へ」を押します。
 
![img](img/windows_xp_install036.png "img")

これでOSインストールは完了です。
OSのディスクを取り出してください。
 
![img](img/windows_xp_install037.png "img")

引き続き、OSの初期設定に進みます。

![img](img/windows_xp_install038.png "img")

[目次に戻る](../)
