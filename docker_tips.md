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

sudo apt-get install docker-ce docker-ce-cli containerd.io
sudo groupadd docker
sudo usermod -a -G docker $USER
sudo systemctl restart docker.service
sudo apt install docker-compose
docker-compose --version
sudo apt purge docker-compose
sudo apt install docker-compose
docker-compose --version
docker ps
```

<h3>Check Docker Images, and add Apache Image</h3>

```
docker ps -- check processes
docker image ls -- check images
docker pull httpd -- pull standard Apache webserver image
```

<h3>Build and inspect Containers</h3>

```
docker build -t <Container-Name> . -- init container
docker run -d --name <Container-App-Name> -p 8080:80 <Container-Name> -- run container
docker ps
docker inspect
docker inspect <Container-App-Name> 
```
<h3>Docker SSH</h3>

```
docker exec -it <Container-App-Name>  /bin/sh
```

<h3>Stop Docker Containers</h3>

```
docker stop <Container-App-Name>  -- stop container
docker stop $(docker ps -a -q) -- stop all containers
docker rm $(docker ps -a -q) -- remove all containers
```
