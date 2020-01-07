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
