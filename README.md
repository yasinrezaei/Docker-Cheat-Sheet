## `Docker Cli`

```bash
docker version
docker help
```

## ` commands`

#### `run,start and restart`
```bash
docker < management commands > < sub commands > < option >

docker container run --name webhost-1 -p 8080:80 nginx:latest

--detach -d
--publish -p


docker container start <container_name>
docker container restart <container_name>
```

#### `list of containers`
```bash
docker container ls 
docker container ls -a 

```

#### `stop and delete containers`
```bash 
docker container stop <container_name>
docker container rm <container_name>
docker container rm -f <container_name>

docker container prune => remove all stoped containers

```


#### `logs`
```bash
dockr container logs <container_name>
dockr container logs -f <container_name>
```

#### `rename`
```bash
docker container rename <container_name> <new_container_name>
```

#### `detail of container`
```bash
docker container port <container_name>
docker container inspect <container_name>
docker container top <container_name> => list of process_id for this container

docker container stats <container_name>


```

