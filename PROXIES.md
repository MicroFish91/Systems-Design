# Proxies

A proxy server is a server application that acts as an intermediary between a client requesting a resource and the server providing that resource.

## Forward Proxy

- A forward proxy is a server that acts on behalf of the client (or set of clients) (e.g. VPN services)
- Often assumed as just "proxy"

## Reverse Proxy

- Reverse proxies act on behalf of a server in a client server interaction (e.g. Nginx)
  - It can filter out requests that you want to ignore
  - Logging
  - Metrics
  - Cache stuff
  - Load Balancing

## Load Balancer

- A load balancer is a device that acts as a reverse proxy and distributes network or application traffic across a number of servers. Load balancers may also serve other secondary functions as described above in the reverse proxy section

- Server selection strategies... any combination of:

  - Round Robin
  - Weighted Round Robin
  - Performance Based
  - Path Based or other application specific data

- You can have load balancers between client and server, server and db, etc.
