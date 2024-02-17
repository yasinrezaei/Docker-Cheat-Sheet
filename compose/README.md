## Docker Compose
```bash
version: ""
services:
    service_name_1:
        container_name:name_1
        image: myimage:latest
        ports:
            - yy:xx
            - ...
        command: ...
        environment:
            - MY_ENV_VARIABLE: 12345
            ...
        volumes:
            - data:/var/lib/data
            - ...
        restart: always
        depends_on:
            - service_name_2
        networks:
            - my_net


    service_name_2:
        container_name:name_2
        ...

volumes:
    data:
        external=True # error if volume does not exists

networks:
    my_net:
        driver: bridge
        name: my_name
```

#### up/down
```bash
docker compose up
docker compose -f anothercompose.yml up

docker compose down
docker compose down -v
docker compose pause/restart/start/stop
```
#### monitoring
```bash
docker compose top
docker compose ps
docker compose logs
docker compose logs -f
docker compose -t # with time stamp
docker compose config # validate
docker compose images # list of images used in this compose

```

#### scaling
```bash
docker compose scale service_1=2 service_2=3
```
