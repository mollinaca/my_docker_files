
# cAdvisor

https://github.com/google/cadvisor  

## docker container

最新のイメージはコチラから  
https://console.cloud.google.com/gcr/images/google-containers/GLOBAL/cadvisor?gcrImageListsize=10  
※ dockerhub のほうは DEPRECATED  

## houw to use

### prepare

https://qiita.com/suzukihi724/items/c4912fce9833dcd9c6bd
```
# sudo mount -o remount,rw '/sys/fs/cgroup'
# sudo ln -s /sys/fs/cgroup/cpu,cpuacct /sys/fs/cgroup/cpuacct,cpu
```


```
# docker pull gcr.io/google-containers/cadvisor:v0.xx.x
# docker-compose up -d
 -> up
# docker-compose ps 
  Name                Command                  State               Ports
---------------------------------------------------------------------------------
cadvisor   /usr/bin/cadvisor -logtostderr   Up (healthy)   0.0.0.0:8080->8080/tcp
```

access to `http://<IPAdress>:8080`
