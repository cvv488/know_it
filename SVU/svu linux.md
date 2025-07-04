# старое имя контейнера в dotnet

./inm_it.sh
Error response from daemon: No such container: svu_inmodule
Error: No such container: svu_inmodule
Unable to find image 'dotnet:6' locally
docker: Error response from daemon: Get "https://registry-1.docker.io/v2/": net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers).
See 'docker run --help'.
Error: No such container: svu_inmodule

- docker tag  log_app:6.0 dotnet:6

добавился:
- docker images
REPOSITORY                               TAG          IMAGE ID       CREATED        SIZE
dotnet                                   6            5e81ee2405c9   2 years ago    217MB
log_app                                  6.0          5e81ee2405c9   2 years ago    217MB





#  tty\Moxa00.. accsess denied - решено
после обновления РГК Астрахань har2 - tty\Moxa00.. accsess denied у всех
изза прав
позв КузнецовуС  он поставил добавил в har2*.sh --privileged \

```sh
#!/bin/bash

docker stop svu_harvester_2;docker rm svu_harvester_2

docker run -dt --net=host --name svu_harvester_2 \
    --privileged \
    -v '/opt/SVU/:/SVU/' \
    -e TZ=Europe/Moscow \
	--restart=always  \
	dotnet:6

#docker exec -dt svu_harvester_2 dotnet /SVU/har2/harvester/HarvesterService.dll 2
docker exec -dt svu_harvester_2 /SVU/har2/harvester/HarvesterService 2
```
