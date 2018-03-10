# 各種ＤＢ環境を作る

### 目的
<pre>
  ・手軽にＤＢ作成、破棄ができること
  ・テーブル作成などの操作が簡単にしたい
  ・でも容量は軽くしたい
</pre>
___

### やったこと
<pre>
  DB構築：docker-compose
  DB操作：adminer
  メンテ・軽量化：busybox
</pre>
___

### インストール
  `git clone https://github.com/covemause/docker_db_box.git`

___

### 構成
~~~
./docker_db_box
    |- docker-compose.yml
~~~

<img src="https://github.com/covemause/documents/blob/master/docker_db_box_image.JPG" />

___

### 起動
  `docker-compose up -d`

___

### adminer画面
`http://{IP}:8080`

<img src="https://github.com/covemause/documents/blob/master/adminer_demo.JPG" />

___

### ログイン
 docker-compose.ymlに記載した情報になります。
 
 |SYSTEM|Server|UserName|Password|Database|
 |:---:|:---:|:---:|:---:|:---:|
 |MySQL|mysql_db|demo|demo|testdb|
 |PostgresSQL|postgres_db|demo|demo|testdb|

___

### Adminer(docker)の日本語化
 イメージ取得のデフォルトが軽量な英語版なので、各国語対応版にする。
 （もっと簡単な方法があれば変更します）

#### 1.コンテナに入る
~~~
 # docker exec -it adminer_box /bin/sh
 /var/www/html $
~~~

#### 2.英語版のadminer.phpを削除する
~~~
/var/www/html $ rm -rf adminer.php
/var/www/html $ ls
designs            plugin-loader.php  plugins-enabled
index.php          plugins
~~~

#### 3.各国語対応のadminer.phpをダウンロードする
~~~
 /var/www/html $ curl -fsSL https://github.com/vrana/adminer/releases/download/v4.6.2/adminer-4.6.2.php -o adminer.php
 /var/www/html $ ls
adminer.php        index.php          plugins
designs            plugin-loader.php  plugins-enabled
~~~

#### 4.コンテナを抜ける
~~~
/var/www/html $ exit
~~~


<img src="https://github.com/covemause/documents/blob/master/adminer_demo_jp.JPG" />
