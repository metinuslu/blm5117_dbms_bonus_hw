# MongoDB Community Server 6

## Install MongoDB with Docker Compose
    > docker-compose up -d

    > docker ps
    > docker-compose ps

    > docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_name_or_id>

## Docker Commands
> docker-compose up -d  
> docker ps or docker compose ps  
> docker-compose down  
> docker-compose logs <CONTAINER_NAME or CONTAINER_ID>  


## Connection
### Terminal
    - docker exec -it mongodb_cs6 mongosh mongodb://root_user:root_pass@localhost:27017 --username root_user --authenticationDatabase admin

### Client with Connection String:
    - mongodb://root_user:root_pass@localhost:27017/ 

## Contact
    - 235B7014 - Metin Uslu