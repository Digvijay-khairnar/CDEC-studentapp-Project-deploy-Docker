# CDEC-studentapp-Project-deploy-Docker
CDEC-studentapp project deploy using docker containers .this is a 3 tier application for practice cloud and devops


# DOCKER INSTALLTION

insall from documentation 

link 
            https://docs.docker.com/engine/install/ubuntu/



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



