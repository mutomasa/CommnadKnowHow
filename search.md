# 検索系のコマンド

### pyファイルから test_functionを検索
find . -name '*.py' | xargs grep test_function

### 2日以上古い過去のファイルを検索 find -mtimeの使いかた
+2 2日以上古い
-2 2日前までの新しいファイル
2 2日前
-daystart オプションを付けると、現在時刻でなく、0:00を基準に計算する

find /var/log/dev/ -type f -mtime +3 | xargs ls -l

### Cのソースでprintfを含む行と、ファイル名を表示する
-R 再帰オプション
-n 行番号表示

grep -n -R "printf" *.c .

### egrepで正規表現
egrep 'Sunday|Monday' error.log


### プロセスからプロセスIDを取得してKillする
pgrep -f 'runserver' | xargs kill 2>/dev/null