```bash
tan@Tan:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS     NAMES
f3d78c407eff   ubuntu    "sh -c 'while true; …"   54 minutes ago   Up 54 minutes             elegant_mcclintock
tan@Tan:~$ docker pull devopsdockeruh/simple-web-service:alpine
alpine: Pulling from devopsdockeruh/simple-web-service
Digest: sha256:dd4d367476f86b7d7579d3379fe446ae5dfce25480903fb0966fc2e5257e0543
Status: Image is up to date for devopsdockeruh/simple-web-service:alpine
docker.io/devopsdockeruh/simple-web-service:alpine
tan@Tan:~$ docker images
REPOSITORY                          TAG       IMAGE ID       CREATED       SIZE
ubuntu                              latest    278628f08d49   4 weeks ago   117MB
devopsdockeruh/simple-web-service   ubuntu    d44e1dce3987   3 years ago   126MB
devopsdockeruh/simple-web-service   alpine    dd4d367476f8   3 years ago   24.3MB
tan@Tan:~$ docker run -d --name alpine devopsdockeruh/simple-web-service:alpine
7717cd69d6d7b5151f490f74783f8a5ec0af794cb105a070ac2eb10b843bf18a
tan@Tan:~$ docker ps
CONTAINER ID   IMAGE                                      COMMAND                  CREATED          STATUS          PORTS     NAMES
7717cd69d6d7   devopsdockeruh/simple-web-service:alpine   "/usr/src/app/server"    7 seconds ago    Up 6 seconds              alpine
f3d78c407eff   ubuntu                                     "sh -c 'while true; …"   55 minutes ago   Up 55 minutes             elegant_mcclintock
tan@Tan:~$ docker exec -it alpine sh
/usr/src/app # ls
server    text.log
/usr/src/app # tail -f ./text.log
2024-11-19 14:26:28 +0000 UTC
2024-11-19 14:26:30 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-11-19 14:26:32 +0000 UTC
2024-11-19 14:26:34 +0000 UTC
2024-11-19 14:26:36 +0000 UTC
2024-11-19 14:26:38 +0000 UTC
2024-11-19 14:26:40 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-11-19 14:26:42 +0000 UTC
2024-11-19 14:26:44 +0000 UTC
2024-11-19 14:26:46 +0000 UTC
2024-11-19 14:26:48 +0000 UTC
2024-11-19 14:26:50 +0000 UTC
```