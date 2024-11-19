```bash

tan@Tan:~/usr$ touch text.log
tan@Tan:~/usr$ docker run -d -v "$(pwd)/text.log://usr/src/app/text.log" devopsdockeruh/simple-web-service:alpine
c1e6232169d7b32aa7184c35c5bcb226122d3ac75ed08245fc81daff5d3bae30
tan@Tan:~/usr$ tail -f ./text.log
2024-11-19 17:18:30 +0000 UTC
2024-11-19 17:18:32 +0000 UTC
2024-11-19 17:18:34 +0000 UTC
2024-11-19 17:18:36 +0000 UTC
2024-11-19 17:18:38 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-11-19 17:18:40 +0000 UTC
2024-11-19 17:18:42 +0000 UTC
2024-11-19 17:18:44 +0000 UTC
2024-11-19 17:18:46 +0000 UTC
2024-11-19 17:18:48 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
2024-11-19 17:18:50 +0000 UTC
2024-11-19 17:18:52 +0000 UTC
2024-11-19 17:18:54 +0000 UTC
2024-11-19 17:18:56 +0000 UTC
^C

```