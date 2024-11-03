# Installation of MySQL server, MySQL Workbench and Superset  
## Installation of Docker
- Visit Docker installation documentation for Ubuntu. [Link to Document.](https://docs.docker.com/engine/install/ubuntu/)
- Add user to docker group `sudo usermod -aG docker $USER`.
- We will use `docker-compose` to run different components, i.e., MySQL server, MySQL workbench and Superset.
## Installation of MySQL server  
- Since we are using `docker-compose` to run MySQL server, we need a `docker-compose.yaml` file to run the container for MySQL.  
- Go to the dockerhub documentation for MySQL server. [Link to Document](https://hub.docker.com/_/mysql)
- Find the `... via docker-compose⁠ or docker stack deploy⁠` part in the documentation.
- Create a directory `mkdir -p ~/projects/mysql-server` in your local machine.
- Copy the docker compose config and write it to `~/projects/mysql-server/docker-compose.yaml` using `nano`
- Add Port binds and Volume binds in the `docker-compose.yaml` for access to db and data persistence respectively.
- Run `docker compose up -d` to spin up a mysql-server container.
## Installation of MySQL Workbench
- Since we are using `docker-compose` to run MySQL Workbench, we need a `docker-compose.yaml` file to run the container for MySQL Workbench.  
- Go to the dockerhub documentation for MySQL Workbench. [Link to Document](https://hub.docker.com/r/linuxserver/mysql-workbench)
- Find the `Usage` part in the documentation.
- Create a directory `mkdir -p ~/projects/mysql-workbench` in your local machine.
- Copy the docker compose config and write it to `~/projects/mysql-workbench/docker-compose.yaml` using `nano`
- Add Port binds and Volume binds in the `docker-compose.yaml` for access to db and data persistence respectively.
- Run `docker compose up -d` to spin up a mysql-workbench container.
## Installation of Superset
- Since we are using `docker-compose` to run Superset, we need a `docker-compose.yaml` file to run the container for Superset.  
- Go to the documentation for installation of Superset. [Link to Document](https://superset.apache.org/docs/installation/docker-compose/)
- Create a directory `mkdir -p ~/projects/superset` in your local machine.
- Follow the steps in the documentation.
- Run `docker compose -f docker-compose-image-tag.yml up -d` to spin up a mysql-workbench container.
