
# about this docker image

Python3.6.8 Environment  
FROM python:3.6.8
https://hub.docker.com/_/python?tab=tags&page=1&name=3.6.8  

### pull official image

```
$ docker pull python:3.6.8
```

### build & container start

```
$ docker-compose up -d --build
```


### container start

```
$ docker-compose start
```

### login to container

```
$ ./exec.sh
```

### push image to Docker.hub

```
$ docker push mollinaca/personal:python368
```
