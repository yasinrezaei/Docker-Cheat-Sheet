## `Docker Cli`

#### `To run Docker without root privileges`
```bash
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker

+ docker context use default
```


```bash
docker version
docker help
```

## ` commands`

#### `run,start and restart`
```bash
docker < management commands > < sub commands > < option >

docker container run --name webhost-1 -p 8080:80 nginx:latest


| Flag          | Short   |
| ---------     | ------- |
| --detach      |   -d    |
| --publish     |   -p    |
| --environment |   -e    |

 


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

docker container inspect <container_name>
docker container inspect -f {{.NetworkSettings.Networks.bridge.IPAdress }} <container_name>

docker container inspect -f {{.NetworkSettings.Networks.bridge.IPAdress }} $(docker container ls -aq)

```


#### `Interactive`

```bash
docker exec -it <container_name> bash

```

#### `Monitoring`

```bash

docker container inspect <CONTAINER_NAME>
docker container inspect -f {{.Config.Entrypoint }} <CONTAINER_NAME>

docker container stats <CONTAINER_NAME> --no-stream 

docker container stats <CONTAINER_NAME> --no-stream 
docker container top <CONTAINER_NAME> 

```

#### `Restart on failure`
```bash
docker container update --restart-failure:3 <container_name>
docker cintainer top < container_name >
kill -9 < PID >
docker container kill < container_name > 
```

#### `Copy a file from onr container ro another one`
```bash
docker container cp test.txt <CONTAINER_NAME>:/oot/test.txt
```

#### `pause and unpause containers`
```bash
docker container pause <CONTAINER_NAME>
docker container unpause <CONTAINER_NAME>
```