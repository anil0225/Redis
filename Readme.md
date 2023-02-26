Redis is an in-memory store
In this repo we create a docker-compose with following Redis Components
- Redis Master: For read and write
- Redis Slave: For replica and read
- Redis Sentinel: Monitor Master and perform switch over when a master fails

Common Redis Commands:
``` 
# on Redis nodes master/slave
redis-cli
info 
info replication 
# on Sentinel
redis-clip -p <<sentinel port e.g 26379>>
info
info sentinel
sentinel masters
sentinel master mymaster
sentinel slaves mymaster
# Force failover
sentinel failover mymaster

```
