Search images in repo:
```
docker search omd
```

To pull images from repo:
```
docker pull cmon2k/docker-centos-omd
```

To list images:
```
docker images
```

Run a command in an image
```
docker run cmon2k/docker-centos-omd  /bin/bash
```

Run a container in daemon mode(background):
```
docker run -d -i -t --name OMD001 cmon2k/docker-centos-omd
```

List containers
```
docker ps
```
List all the Docker containers:
```
docker ps -a
```

Stop a container:
```
docker stop furious_meitner
```

Start a container:
```
docker start angry_engelbart
```

Remove a container:
```
docker rm furious_meitner
```

Attach to a container:
```
docker attach jovial_carson
```
Detach from a container:
```
# To detach the tty without exiting the shell,
# use the escape sequence Ctrl-p + Ctrl-q
```

#### Basic understanding of images and containers:
```
http://docs.docker.com/terms/image/
http://docs.docker.com/terms/layer/
http://docs.docker.com/terms/container/
```

If you want the container to be saved into image you can use “docker commit” to push the image to repo.

Saving container as image:
```
docker commit <continer id> rahulnai/test:1.0 (this saves container as image)
```

Connecting to container:
```
root@ubuntu14:~/test# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                     NAMES
2a7082a4c964        tomcat:7            "catalina.sh run"   2 days ago          Up 2 days           0.0.0.0:32768->8080/tcp   cocky_brattain

root@ubuntu14:~/test# docker exec -it 2a7082a4c964 bash
```

Push the images to repository:
```
docker push rahulnai/test:1.0
docker tag rahulnai/test:1.0 sometaginrepo/someinrepo:1.0
```

DOCKER OPERATIONS:
```
docker  logs <container name>
```

Logs:
```
docker  -d --log-level =debug
```

The “inspect“” command will list the complete information of the container
```
docker inspect 52249ba75f0f
```


