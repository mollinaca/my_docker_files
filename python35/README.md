
# about this docker image

Python3.5 Environment  
FROM python:3.5
https://hub.docker.com/_/python?tab=tags&page=1&name=3.5

### pull official image

```
$ docker pull python:3.5
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
$ docker push mollinaca/personal:python35
```
