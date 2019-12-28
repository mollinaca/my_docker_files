
# about this docker image

Python3.4.3 Environment
FROM python:3.4.3

### build & container start

```
$ docker-compose up python343
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
$ docker push mollinaca/personal:python343
```
