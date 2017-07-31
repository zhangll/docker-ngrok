# DOCKER NGROK IMAGE

## BUILD IMAGE

```linux
git clone https://github.com/hteen/docker-ngrok.git
cd docker-ngrok

docker build -t zhangll/ngrok .

docker run --rm -it -e DOMAIN="k.bestsrc.com" -v /data/ngrok:/myfiles zhangll/ngrok /bin/sh /build.sh

docker run -idt --name ngrok-server \
-v /data/ngrok:/myfiles \
-p 8090:80 \
-p 4438:443 \
-p 4209:4443 \
-e DOMAIN='k.bestsrc.com' zhangll/ngrok /bin/sh /server.sh

```
