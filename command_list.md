# よく業務で使用するコマンド

## [ps]プロセスがいるかどうか
+ `ps -ef | grep [プロセス名]`

## [netstat]ポートが空いているかどうか
+ `netstat -na | grep [ポート番号]`

## [netstat]ポートが使用しているプロセス名を確認する時
+ `netstat -ntlp | grep [ポート番号]`

## [grep]ファイルの中の特定文字を抽出したい時
+ `cat [ファイル名] | grep [検索条件]`
* `cat /etc/hosts | grep 192.168.1.1`

## [grep]カレントディレクトリ配下のファイル全てに対して特文字を抽出したい時
+ `grep -r [検索条件]`

## [awk]コマンド実行結果の何カラム目かを抽出する時
+ `ls -lR roles/*/*/*.yml | awk -F ' ' '{print $9}'`
+ `https://qiita.com/yamazon/items/563af1b485ff413d381f`

## [sort]コマンド実行結果の何カラム目かで並び替える時
+ `ls -lR roles/*/*/*.yml | sort -k 4r`
+ `https://www.atmarkit.co.jp/ait/articles/1611/09/news020.html`

## [sort]プロセスのメモリ使用率が高い順に並び替える時
+ `ps aux --sort rss`

## [sed]ファイルの中に記載されている文字列を置換したい時
+ `sed -e 's/[検索文字列]]/[置換文字列]]/g' [ファイル名]]`
+ `https://qiita.com/hirohiro77/items/7fe2f68781c41777e507`

