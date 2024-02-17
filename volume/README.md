## Volume
```bash
docker image inspect <image_name> => List of volumes are here that this image use

docker volume ls
docker volume inspect <volume_name>

docker volume rm <volume_name>

docker volume prune

docker container --name <container_name> -v mysqldb1:/var/lib/mysql <image_name>

```

## Bind Mounts
```bash
docker container run --name <container_name> -p x:x --mount type=bind,source=/root/projects/data,target=/app <image_name> 

```
