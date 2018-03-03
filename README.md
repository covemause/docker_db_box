# Adminerを使ってMysql, Postgresqlをサクッと作る

### インストール
  `git clone https://github.com/covemause/docker_db_box.git`


### 構成
~~~
./docker_db_box
    |- docker-compose.yml
~~~


### 起動
  `docker-compose up -d`


### adminer画面
<img src="https://github.com/covemause/docker_db_box/blob/master/adminer_demo.JPG" />


### ログイン
 docker-compose.ymlに記載した情報になります。
 
 |SYSTEM|Server|UserName|Password|Database|
 |:---:|:---:|:---:|:---:|:---:|
 |MySQL|mysql_db|demo|demo|testdb|
 |PostgresSQL|postgres_db|demo|demo|testdb|
