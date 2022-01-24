# Scaling

| Horizontal                | Vertical                   |
| ------------------------- | -------------------------- |
| Load Balancing Required   | N/A                        |
| Resilient                 | Single Point of Failure    |
| Network Calls             | Interprocess Communication |
| Data Inconsistency        | Consistent                 |
| Scales well w/ inc. users | Hardware Limit             |

In real world we may use a combination of the two.

## Improving a System

- Optimizing processes and increasing throughput using the same resources (vertical scaling)
- Preparing beforehand at non-peak hours (preprocessing/cron-jobs)
- Adding backups (increase resilience)
- Buying more machines (horizontal scaling)
- Micro-service architecture
- Distributed system (partitioning)
- Load Balancer
- Decoupling
- Logging & Metrics

## Home

- [Home](./README.md)
