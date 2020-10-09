# 検索系のコマンド

### pyファイルから test_functionを検索
find . -name '*.py' | xargs grep test_function

### 一致したファイルのみ表示
-r 再帰検索
-l 一致したファイルのみ表示

### プロセスからプロセスIDを取得してKillする
pgrep -f 'runserver' | xargs kill 2>/dev/null