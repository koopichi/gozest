# gozest

1. Install Docker
```bash
bash <(curl -Ls https://raw.githubusercontent.com/koopichi/ocserv/master/dk.sh)
```
2. Build docker image
```bash
docker build -t gozest https://github.com/koopichi/gozest.git
```

3. Run docker container
```bash
docker run -d -p port --net=host gozest gost -D -L=tcp://:port/destip:destport
```
4. Set container to run at Startup
```bash
docker update --restart unless-stopped $(docker ps -q)
```
