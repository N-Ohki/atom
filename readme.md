# GitHubでatom設定管理メモ

## インストールパッケージの共有
1. `.atom` ディレクトリにパッケージリストを作る

    `$ apm list --installed --bare > packages.txt`

2. 「パッケージリスト」に記載のパッケージをインストールする

    `$ apm install --packages-file packages.txt'`

※詳しくはこちら↓
http://mae.chab.in/archives/2605

## 拡張子関連付け方法

- `.atom/atom.exe` をatomで起動したい拡張子に関連付けする
- アップデートの度関連付けが削除されないよう%LocalAppData%\atom\atom.exeには指定しないこと
- windowsにて関連付けができない場合の対処法は以下

Windows7 にて。「ファイルを開くプログラムの選択」で「参照」を押下し、任意のプログラムを選んでも一覧に追加されない不具合の解消法。

以下の手順で解消可能。

レジストリエディタ `regedit` を開く
`HKEY_CLASSES_ROOT\Applications\` まで移動しツリーを開く
一覧に追加されないプログラムのキー (例の場合で言えば atom.exe) とそのサブキーを全て削除する

これで完了。もう一度「ファイルを開くプログラムの選択」でそのプログラムを選択すれば一覧に追加される。

参考：http://nanpanyblog.jpn.ph/?p=304
