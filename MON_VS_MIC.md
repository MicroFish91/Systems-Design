# Monolith vs. Microservice Architecture

A software system is monolithic if it has functionally distinguishable aspects that are all interwoven, rather than containing architecturally separate components.

Microservices is both an approach to software architecture that builds a large, complex application from multiple small components which each perform a single function and is the term for the small components themselves.

| Monolith                                | Microservice                                       |
| --------------------------------------- | -------------------------------------------------- |
| Good for a small cohesive team          | More teams to manage separate codebases            |
| Less Complex                            | More Complex                                       |
| Less Code Duplication                   | May have repeat code (for tests, connections, etc) |
| Faster, in-the-box calls                | Slower, separate pieces / network calls            |
| Harder to grasp for new members         | Less understanding is required of the full system  |
| Less Resilient, Single Point of Failure | More Resilient, Decoupled Responsibilities         |
| Harder to Scale                         | Easier to Scale                                    |
| Harder to Parallel Develop              | Parallel development is easier                     |
| Harder to monitor services              | Easier to see which services are used most often   |

Stack overflow still uses a monolith architecture. Many big companies like Google and Facebook uses microservice architecture.

## Home

- [Home](./README.md)
