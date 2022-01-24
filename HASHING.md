# Hashing (w/ context of Load Balancing)

General concept (not yet implementing consistent hashing):

1. A client makes a request, the request has a requestId (Request ID usually encapsulates some information about the User. For example User ID.)
2. Hash the requestId using a hash function
3. Map that hash to the server by dividing by n servers

## Hashing vs. Round Robin

Firstly, why use hashing over round robin => because the same input will always give us the same output (i.e. user will hit the same server each time). In this way, we can save time via local server cache from a previous hit which saves overall system time.

A good hash function will ensure that the overall distribution is random but evenly distributed. A round robin strategy will not have the benefit of uniform distribution while ALSO hitting the same server to the same users.

## Consistent Hashing

The issue that is presented comes when we add or remove servers. We end up with the possibility that a previous user will now not go to the same server as before, so we lose a lot of overall system time that was being saved via local server cache hits. Basically Rehashing is expensive. The solution is consistent hashing.

Consistent Hashing is a distributed hashing scheme that operates independently of the number of servers or objects in a distributed hash table by assigning them a position on an abstract circle, or hash ring. This allows servers and objects to scale without affecting the overall system.
