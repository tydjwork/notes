[toc]

### run docker on win10

1. install docker
2. install git
3. install vscode for terminal (+powershell)

#### mount volume permission error; need to do 'docker run' on powershell

```
C:\Program Files\Docker\Docker\resources\bin\docker.exe: Error response from daemon: mkdir C:\Program Files\Git\var: Access is denied.
See 'C:\Program Files\Docker\Docker\resources\bin\docker.exe run --help'.
```

### portainer

```
docker run -d \
-p 9000:9000 \
-p 8000:8000 \
--name portainer \
--restart always \
-v /var/run/docker.sock:/var/run/docker.sock \
-v /d/docker/portainer:/data \
portainer/portainer
```

### centos

```
docker run -d \
--restart always \
--name=centos \
centos:7 sleep infinity
```

