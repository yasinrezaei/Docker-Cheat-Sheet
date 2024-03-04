## Swarm
- load balancing between servers
- availability
- automate container running
- add or remove containers
- update systems without downtime
- rolling update for containers
  
---

- Nodes:
    - managers
    - workers
  
---
Raft Database(internal distributed state store between managers node)

---
- swarm manager
   - docker service create
   - API (accept commands and create service object)
   - orchestrator (create tasks for service objects)
   - allocator (allocate IP address to tasks)
   - dispatcher (assign tasks to nodes)
   - scheduler (instruct a worker to run a task)
 - worker node
   - worker (connects to dispatcher to check for assigned tasks)
   - executer (executes tasks assigned to worker node)

---

## Swarm cluster
```bash

docker info
docker swarm init
docker swarm init --advertise-addr=IP
docker swarm leave
docker swarm leave --force

docker swarm join-token manager
docker swarm join-token worker

docker node ls # ( in manager nodes)
docker node promote < WORKER_NAME >
docker node demote < WORKER_NAME >

docker service create --name < SERVICE_NAME > --replicas <REPLICA_COUNT> <IMAGE> <COMMAND>

docker service ls 
docker service ps <SERVICE_NAME>

docker node ps # containers on each manager node
docker node ps <NODE_NAME>
docker container ls # for worker nodes

docker service logs -f < SERVICE_NAME >

docker service rm < SERVICE_NAME > # swarm doesnt have stop service

docker service update < SERVICE_NAME > --replicas <NEW_REPLICA_COUNT>


```
