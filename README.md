tsselect for Linux, Windows, macOS, BSD, etc.

1. 目標
 marumo氏のtsselectのLinuxへのポート。車輪の何度目かの再開発

2. 変更点
 以下の機能を追加
 - 入力または出力に "-" を指定すると標準入出力とみなす
 - 同期エラーだけでなく連続性指標によるドロップ検出部分も "resync[n](drop only) :" として報告
 - 9個以上の同期エラーもすべて詳細表示
 - 同期エラー報告時、前後のTDT/TOT時刻が得られていれば "time : 前時刻, 後時刻" として表示
   (ファイル先頭などで前後どちらかの時刻が不明のときは "--" になる)

3. TurtleWilly's Changes
 - More spacing in the output (I deal with large files)
 - More descriptive labels
 - In case of issues (drops, errors) mark things in 'red' color (can be
   disabled with NO_COLOR environment variable)

![tsselect in action](screenshot.png)