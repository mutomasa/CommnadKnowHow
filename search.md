# 検索系のコマンド

### 一致したファイルのみ表示
-r 再帰検索
-l 一致したファイルのみ表示

### プロセスからプロセスIDを取得してKillする
pgrep -f 'runserver' | xargs kill 2>/dev/null