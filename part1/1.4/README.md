## terminal 1

```bash
 docker run -it ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'
Unable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu
afad30e59d72: Download complete
Digest: sha256:278628f08d4979fb9af9ead44277dbc9c92c2465922310916ad0c46ec9999295
Status: Downloaded newer image for ubuntu:latest
Input website:
helsinki.fi
Searching..
<html>
<head><title>301 Moved Permanently</title></head>
<body>
<center><h1>301 Moved Permanently</h1></center>
<hr><center>nginx/1.24.0</center>
</body>
</html>
```
## terminal 2
```bash
docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED         STATUS         PORTS     NAMES
f3d78c407eff   ubuntu    "sh -c 'while true; …"   3 minutes ago   Up 3 minutes             elegant_mcclintock

docker exec -it f3d78c407eff bash
apt update
apt install -y curl
```