# docker files for prom and grafana 

docker and cofig files and releated directories.

# how to use

## prepare docker-compose

https://docs.docker.com/compose/install/

## prepare docker images

```
$ docker pull prom/prometheus:v2.15.2 
$ docker pull prom/node-exporter:v0.18.1
$ docker pull gcr.io/google-containers/cadvisor:v0.35.0 
$ docker pull docker.io/grafana/grafana:6.5.2 
```

## how to use this repo

### build docker images

```
$ git clone <this repo>
$ cd <dir>
$ docker-compose up -d --build
 ~~~~~
 ~~~~~
 Creating prometheus       ... done
 Creating grafana          ... done   
 Creating node_exporter    ... done   
 Creating cadvisor         ... done   

```

### access and use

ブラウザで `http://<IPaddress>:3000` → grafana へアクセス、 admin/admin でログインできることを確認  
ブラウザで `http://<IPaddress>:9090` → prometheusへアクセスできることを確認  

grafanaへログインし、Add data source → prometheus → http://<IPaddress>:9090 を追加 → Save & Test → 追加されることを確認  

# update docker image version or config files

いずれもコンテナまるごとリビルド  
コンテナイメージを最新化する場合は、 docker pull で最新イメージを持ってきて、各 Dockerfile の `FROM: ` を書き換える  
configを更新する場合は、各configを更新して、リビルドすればよい

```
$ docker-compose up -d --build
```

promethes, grafana のステートフルなデータは、attach された voluem に永続化されるので、
コンテナ作り直してそのまま閲覧できる（もちろん、アプリケーション側でのバージョン変更による互換性の維持は必要）

# Todo

* 監視対象のアプリケーション用コンテナイメージの中に node_exporter、および必要な exporter を用意
  * node_exporter はいらんかな
  * それらを監視できるように、 prometheus.yml の調整

* grafana.ini の調整
  * Listenポートを443へ変更
  * https 化、SSL証明書（独自証明書？正規（LetsEncryptなど）とる？）
  * DNSについて確認
