# 抽出系のコマンド

### 3つめのフィールド以上を取り出す (先頭行削除)
ps | sed -e '1d' | cut -d ' ' -f3-

### 先頭行をスキップして、フィールドを取り出す
ps  | awk  'NR>1{print $1}'

### ディスクの空き容量　sortでフィールド指定　
df | sort -k 2rn

### sedの範囲指定を使って、ログを抽出　
cat /var/log/apache2/access_log | sed -n '/02\/May\/2014:22/,/02\/May\/2014:23/p

### awkで日付範囲で抽出
cat error_log | awk '$3>="08:12:40" && $3<"08:13:50"'

### secureからsshdを抽出
awkで正規表現
cat secure | awk '$5 ~/sshd[[0-9]*]:/'
