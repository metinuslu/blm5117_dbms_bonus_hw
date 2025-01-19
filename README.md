# MongoDB Community Server 6

## Alternative -1 :Install MongoDB with Docker
Pull Image               : docker pull mongodb/mongodb-community-server:latest
with Restart Container   : 
docker run  -d -p 27018:27018 -e MONGO_INITDB_ROOT_USERNAME=root_user -e MONGO_INITDB_ROOT_PASSWORD=root_pass -v ./mongodb_data2_1:/data/db --restart always --name mongodb_cs_cont_2_1 mongodb/mongodb-community-server:latest
with Remove Container    : 
docker run --rm -d -p 27019:27019 -e MONGO_INITDB_ROOT_USERNAME=root_user -e MONGO_INITDB_ROOT_PASSWORD=root_pass -v ./mongodb_data2_2:/data/db --name mongodb_cs_cont_2_2 mongodb/mongodb-community-server:latest

docker run -d -p 27017:27017 --name mongodb -v ~/mongo-data:/data/db mongo

> docker exec -it mongodb_cs6 mongosh
> docker exec -it mongodb_cs6 mongosh mongodb://root_user:root_pass@localhost:27017 --username root_user --authenticationDatabase admin


mongosh "mongodb://mongodb0.example.com:28015" --username alice --authenticationDatabase admin


## Alternative -2: Install MongoDB with Docker Compose
    > docker-compose up -d

    > docker ps
    > docker-compose ps

    > docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_name_or_id>

## Docker Commands
docker-compose up -d: Bu komut ile MongoDB container'ını arka planda çalıştırırsın.
docker-compose down: Bu komut ile MongoDB container'ını durdurursun.
docker-compose logs mongodb: Bu komut ile MongoDB container'ının loglarını görürsün.