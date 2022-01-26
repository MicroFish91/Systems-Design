# Systems Design Considerations

1. [Horizontal vs. Vertical Scaling](./SCALING.md)
2. [Measuring System Performance](./SYS_PERF.md)
3. [Measuring System Availability](./SYS_AVAIL.md)
4. [Proxies](./PROXIES.md)
5. [Load Balancing](./PROXIES.md#load-balancer)
6. [Consistent Hashing](./HASHING.md)
7. [Monolith vs. Microservice Architecture](./MON_VS_MIC.md)
8. [Caching](./CACHING.md)
9. [Database Sharding](./SHARDING_PARTITION.md)

## Message Queue

- Servers are processing jobs in parallel.
- A server can crash. The jobs running on the crashed server still needs to get processed.
- A notifier constantly polls the status of each server and if a server crashes it takes ALL unfinished jobs (listed in some database) and distributes it to the rest of the servers. Because distribution uses a load balancer (with consistent hashing) duplicate processing will not occur as job_1 which might be processing on server_3 (alive) will land again on server_3, and so on.
- This "notifier with load balancing" is a "Message Queue".
