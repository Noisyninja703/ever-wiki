# Docker Tips

<h3>Check Docker Version</h3>

```
docker --version

docker-compose --version
```

<h3>Remove old versions and reinstall</h3>

```
sudo apt-get remove docker docker-engine docker.io containerd runc

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/docker-archive-keyring.gpg

sudo bash -c 'echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" > /etc/apt/sources.list.d/docker.list'

  108  sudo apt-get install docker-ce docker-ce-cli containerd.io
  109  sudo groupadd docker
  110  sudo usermod -a -G docker $USER
  111  sudo systemctl restart docker.service
  112  sudo apt install docker-compose
  113  docker-compose --version
  114  sudo apt purge docker-compose
  115  sudo apt install docker-compose
  116  docker-compose --version
  117  docker ps
```

<h3>Check Docker Images, and add Apache Image</h3>

```
docker ps -- check processes
docker image ls -- check images
docker pull httpd -- pull standard Apache webserver image
```

<h3>Build and inspect Containers</h3>

```
docker build -t my-apache2 . -- init container
docker run -d --name my-app -p 8080:80 my-apache2 -- run container
docker ps
docker inspect
docker inspect my-app
```
<h3>Docker SSH</h3>

```
docker exec -it my-app /bin/sh
```

<h3>Stop Docker Containers</h3>

```
docker stop my-app -- stop container
docker stop $(docker ps -a -q) -- stop all containers
docker rm $(docker ps -a -q) -- remove all containers
```
