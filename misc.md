# 種々雑多のコマンドリスト

### ホスト名が書かれたファイルを読んで、SSHログインする
cat ssh_hosts | xargs -I {} ssh user@{} hostname