# Symfony 5 & MongoDB (REST API)
Restaurant Finder

### Pre-required
- Assuming that you have Docker installed on your server.


### Usage
Downloading the MongoDB image, the following command will get the 4.2.5-bionic tag, you can delete if you want get the latest version:
```bash
docker pull mongo:4.2.5-bionic
```

The following command will run the container and map its ports with host ports so that way we can access the database from a host level application. The ports used were taken from the [MongoDB documentation](https://docs.mongodb.com/manual/reference/default-mongodb-port/):

```bash
docker run -p 27017-27019:27017-27019 -d mongo:4.2.5-bionic
```

Verify if the instance is runing:

```bash
docker ps -a
```

Copy the data to MongoDB deployment:
```bash
docker cp restaurants.json [container-id]:/home/restaurants.json
```

The following command will connect to the MongoDB deployment using the interactive terminal and start the bash shell:
```bash
docker exec -it [container-id] bash
```

Import our data:
```bash
cd /home
mongoimport --db [database-name] --collection restaurants restaurants.json
```

