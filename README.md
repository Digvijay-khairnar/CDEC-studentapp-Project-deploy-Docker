# CDEC-studentapp-Project-deploy-Docker
CDEC-studentapp project deploy using docker containers .this is a 3 tier application for practice cloud and devops


# DOCKER INSTALLTION

# 1) Set up Docker's apt repository.

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

# 2)Install the Docker packages.

sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


#  MARIADB INSTALLTION AND CRATE DATABASE
docker run -d -e MARIADB_ROOT_PASSWORD=123 -p 3306:3306 mariadb

# INSDIE THE MARIYA DB CONTAINER 
docker exec -it <CONTAINER-ID> bash

# LOGIN DATABASE
mariadb -uroot -p123

# CREATE THE DATABASE
 CREATE DATABASE student_db;

# VIEW databases
show databases;

# USE DATABASE
use student_db;

# leave the database and container
exit;
exit;



