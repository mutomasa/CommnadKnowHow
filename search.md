# 検索系のコマンド

### pyファイルから test_functionを検索
find . -name '*.py' | xargs grep test_function

### Cのソースでprintfを含む行と、ファイル名を表示する
-R 再帰オプション
-n 行番号表示

grep -n -R "printf" *.c .

### egrepで正規表現
egrep 'Sunday|Monday' error.log


### プロセスからプロセスIDを取得してKillする
pgrep -f 'runserver' | xargs kill 2>/dev/null