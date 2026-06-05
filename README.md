# 🚢Docker-Set-Up
Set up and install Docker Engine from Docker's

- Launch an instance 
- connect to the server
- Edit Security groups: Add port:- all traffic 
- Go to the Docker official website: Docker installation on Ubuntu 
   - https://docs.docker.com/engine/install/ubuntu/
---
## 1. Install using the apt repository
-Before you install Docker Engine for the first time on a new host machine, you need to set up the Docker apt repository. Afterward, you can install and update Docker from the repository.
   - Set up Docker's apt repository.

```
# Add Docker's official GPG key:
sudo apt update
sudo apt install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
sudo tee /etc/apt/sources.list.d/docker.sources <<EOF
Types: deb
URIs: https://download.docker.com/linux/ubuntu
Suites: $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}")
Components: stable
Architectures: $(dpkg --print-architecture)
Signed-By: /etc/apt/keyrings/docker.asc
EOF

sudo apt update
```
---
## 2. Install the Docker packages.
   - To install the latest version, run : select latest
   ```
   sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
   ```
---
## Run Your First Container
-📌pull image name from heare : `mukunddeo9325/super-mario `

- pull images from docker registory
- `docker pull <images name>` to pull the images replace image name as : nginx, httpd, mysql, ubuntu, ...etc
```
docker pull <images name>
```
- `docker run -d -P <imagename/imageID>` to run the container from specific image
```
docker run -d -P <imagename/imageID>
```
- `docker ps` to check all the running container
```
docker ps
```
- `docker images` to check all the images
```
docker images
```
---
- Copy the instance public IP and paste it into the Chrome browser
-![Image Alt Text](https://github.com/vedant-07-git/Docker-Set-Up/blob/aff415bdc7eb393efd91e0c0ab80e93c40f365b4/Screenshot%202026-06-05%20152708.png) 


