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
