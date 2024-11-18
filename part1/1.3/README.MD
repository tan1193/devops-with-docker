![alt text](image.png)

Secret message is: 'You can find the source code here: https://github.com/docker-hy'

# Command 

1. Start the container
```bash
docker run -d --name secret_container devopsdockeruh/simple-web-service:ubuntu
```

2. Access the container

```bash
docker exec -it secret_container bash
```

3. Follow the logs

```bash
tail -f ./text.log
```