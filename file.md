# ファイル操作のコマンド

### ファイルをxargsを使ってコピー
find /root/test -type f -name '*-010000*' | xargs -i cp {} /root

### scpでファイル転送
scp -r pi@remotehost:/remote/dir /local/dir
scp -r /local/dir pi@remotehost:/remote/dir

### ログをファイルに残す
teeで画面に同時に表示する
make 2>&1 | tee make-log 
標準エラーと標準出力を同じファイルに書き出す
make  make-log 2>&1

### リモートファイルとローカルファイルとのdiff
公開鍵認証でないと不可
diff /etc/hosts <(ssh user@remotehost sudo cat /etc/hosts)