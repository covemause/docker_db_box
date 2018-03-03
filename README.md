# 各種ＤＢ環境を作る

### 目的
  ・手軽にＤＢ作成、破棄ができること
  ・テーブル作成などの操作が簡単にしたい
  ・でも容量は軽くしたい

### やったこと
  DB構築：docker-compose
  簡単DB操作：adminer
  メンテ・軽量化：busybox

### インストール
  `git clone https://github.com/covemause/docker_db_box.git`

___

### 構成
~~~
./docker_db_box
    |- docker-compose.yml
~~~

___

### 起動
  `docker-compose up -d`

___

### adminer画面
`http://{IP}:8080`

<img src="https://github.com/covemause/docker_db_box/blob/master/adminer_demo.JPG" />

___

### ログイン
 docker-compose.ymlに記載した情報になります。
 
 |SYSTEM|Server|UserName|Password|Database|
 |:---:|:---:|:---:|:---:|:---:|
 |MySQL|mysql_db|demo|demo|testdb|
 |PostgresSQL|postgres_db|demo|demo|testdb|
