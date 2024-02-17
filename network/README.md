## Network

- docker default network => bridge
- One container can be on more than one network
  

- My Server
  - webservice_net(80:80):
      - mongodb
      - nginx
  - Bridge (8080:80)
      - mysql
      - nginx

## Commands

```bash 

docker network ls
docker network inspect <network_id>

docker network create <network_name>

docker network connect <network_name> <container_name>

docker network disconnect <network_name> <container_name>

docker continer run -d -p 8080:80 --name <container_name> --network <network_name> <image_name>


```

#### DNS 
- container_name => Ip

- IPs are unstable in containers
  