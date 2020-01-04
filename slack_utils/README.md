
# about this docker image

${HOSTNAME} Environment  
FROM XXXXX:XXXXXXX #original image if it's exsits

### pull official image

```
$ docker pull ${ORIGINAL}
```

### build & container start

```
$ docker-compose up ${HOSTNAME}
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
$ docker push mollinaca/personal:${HOSTNAME}
```
