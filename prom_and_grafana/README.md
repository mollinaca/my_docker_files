# docker files for prom and grafana 

docker and cofig files and releated directories.

# how to use

## prepare docker-compose

https://docs.docker.com/compose/install/

## how to use this repo

### build docker images

```
$ git clone <this repo>
$ cd <dir>
$ docker-compose up -d
 ~~~~~
 ~~~~~
 Creating prometheus ... done
 Creating grafana    ... done   
```

### access and use

ブラウザで `http://<IPaddress>:3000` → grafana へアクセス、 admin/admin でログインできることを確認  
ブラウザで `http://<IPaddress>:9090` → prometheusへアクセスできることを確認  

grafanaへログインし、Add data source → prometheus → `http://<IPaddress>:9090` を追加 → Save & Test → 追加されることを確認  
もしここで HTTP Bad Gataway になる場合は、 `#docker inspect <prometheusのコンテナID>` で prometheus のコンテナに割り与えられている IPAddres を確認する  

# Todo

* grafana.ini の調整
  * Listenポートを443へ変更
  * https 化、SSL証明書（独自証明書？正規（LetsEncryptなど）とる？）
  * DNSについて確認

* config など概ね良さそうなら、 is-mmo1 のほうのリポジトリに移す（妻木さんレビューなど） 
* 本番環境のフォルダ構成について検討（現在は暫定、細谷のローカルVM環境上でのテスト構築のみ）
