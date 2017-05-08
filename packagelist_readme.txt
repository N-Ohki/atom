GitHubでatom設定ファイル管理メモ


パッケージリストを作る

$ apm list --installed --bare > packages.txt

「パッケージリスト」に記載のパッケージをインストールする

$ apm install --packages-file packages.txt

詳しくはこちら↓
http://mae.chab.in/archives/2605
