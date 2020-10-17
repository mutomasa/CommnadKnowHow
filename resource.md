# リソース調査系のコマンド

### ディスクの空き容量　sortでフィールド指定　
df | sort -k 2rn

### ディレクトリ単位で使用量上位１０件までを表示
df -k | sort -n | tail -10

### ルートパーティション以下の深さ３までディレクトリサイズ
sudo du --max-depth=3 -x / | sort -nr

### サイズが1M以上のファイル
find ./ -size +1M

