# Adminerを使ってMysql, Postgresqlをサクッと作る

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
