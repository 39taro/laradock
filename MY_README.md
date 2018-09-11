# My_Laradock
自分用Laradockです。
使用しそうなservicesは以下です。
workspace,php-fpm,nginx,mysql,phpmyadmin,redis

Reactも使いたいので、create-react-appをインストールしています。

```
cp env-local .env
```
```
docker-compose up -d workspace nginx php-fpm mysql phpmyadmin redis
```
```
cd ./app
```

## 更新履歴
20180911_1 : mysql5.7起動時にerrorになるのでmy.confに設定追加  
https://github.com/farmOS/farmOS/issues/55
20180911_2 : mysqlをversion5.6に変更


start a development!
## 各servicesとPortまとめ

workspace(80:) : workspace   
php-fpm(:9000) : php-fpm  
nginx(80:) : nginx  
blackfire: PHPプロファイル  
apache(80:80) : web server  
hhvm(9000) : Hack実行用のVM  
Minio(9000:9000) : S3互換のObject Storage  
MySQL(3306:3306) : MySQL  
Percona(3306:3306) : MySQL互換のハイパフォーマンスDBサーバー  
MSSQL(1433:1433) : MSSQL  
MariaDB(3306:3306) : MySQL派生のDBサーバー  
PostgreSQL(5432:5432) : PostgreSQL  
PostgreSQL PostGis(5432:5432) : PostgreSQLの地理情報システムの拡張モジュール  
Neo4j(7474:7474,1337:1337) : グラフデータベース  
MongoDB(27017:27017) : オブジェクト指向データベース  
RethinkDB(8090:8080) : JSON保存できるNoSQL  
Redis(6379:6379) : インメモリ型キーバリュー型データストア (KVS)  
Aerospike(3000:3000,3001:3001,3002:3002,3003:3003) : 超高速NoSQLデータベース  
Memcached(11211:11211) : キャッシュサーバー  
Beanstalkd(11300:11300) : 非同期処理を実行するキューサーバー  
RadditMQ(5672:5672,15672:15672,15671:15671) : メッセージングのミドルウェア  
Beanstalkd console(2080:2080) : Beanstalkd console  
Caddy(80:80,443:443) : HTTP/2 web server  
phpmyadmin(8080:80) : phpmyadmin  
Adminer(8080:8080) : DB管理画面  
pgAdmin(5050:5050) : postgre管理画面  
elasticSearch(9200:9200,9300:9300) : elasticSearch  
kibana(5601:5601) : kibana  
Certbot : Let's encrypt暗号化を自動で実行するソフトウェア。HTTPSにする。  
Mailhog(1025:1025,8025:8025) : メール送受信サーバー  
MailDev(1080:80,25:25) : メール送受信サーバー  
Selenium(4444:4444) : Selenium  
Jenkins(8090:8080,50000:50000) : CI  
Grafana(3000:3000) : モニタリングツール  
Laravel Echo Server(6001:6001) : Laravelのブロードキャスト機能用のSocket.io Server  
Solr(8983:8983) : 全文検索システム  
AWS EB CLI : AWS elastic Beanstalkd CLI  
Portainer(9010:9000) : DockerのためのSimple Management  
Gitlab(8989:80,9898:443,2289:22) : Gitlab  
Jupyterhub(9991:80) : Jupyterhub  
IPython(33327-33338:33327-33328) : 対話的Pythonシェル  
Docker-in-Docker(2375) : docker:dind  
NetData(19999:19999) : リアルタイムのリソースモニタリング  
PHPRedisAdmin(9987:80) : Redisデータベースソフトウェア  
MongoWebUI(3000:3000) : MongoWebUI  
Metabase(3030:3000) : データベース解析・グラフ化ツール  

## 使いそうなserviceメモ
workspace(80:) : workspace  
php-fpm(:9000) : php-fpm  
nginx(80:) : nginx  
MySQL(3306:3306) : MySQL  
phpmyadmin(8080:80) : phpmyadmin  
Redis(6379:6379) : インメモリ型キーバリュー型データストア (KVS)  
