# ServerStatusDocker
 Official Docker Version of Server Status.

### Mmm, What do I use this for?

```
You can use this in case if you want an isolated installation but you don't have extra computing resources for a a vm.
You may also prefer this if you are having dependency problems and for development.
```

### How do I use it?

```
You can use it by running this container.
We recommend using a reverse proxy in this case (eg. nginx)

Ports:
Server Status Web App - 4000
MYSQL Server - 4500 (inside requests are still on port 3306)
Database Admin - 4600
```



### How do I run this container?

```shell
# Go to Server Status's Docker Version's Directory
cd SkyMakeDocker
# Make sure you can see the docker-compose file
# Compose the docker install
docker-compose up
# Don't forget to CHANGE the MYSQL Password inside docker-compose.yml file
```

#### Based on Skyfallen SkyMake Container Architecture
