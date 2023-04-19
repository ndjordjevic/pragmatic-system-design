## Diagram building blocks
1. Service as box, double box means multiple services behind the Load balancer
2. User (who might send a request) could be drawn as a user icon
3. Network divider, a dotted line divides Users and the System and represent a network and will be a good thing to put a protocol it uses (HTTP for example)
4. Databases a barrel with a name of the DB type used
5. Synchronous channel a http call for example (user makes a call to the service), a solid line with an arrow with a format of a URL if it's a REST request (GET /user/:id for example)
6. Queue, a dotted line
## Tips on building good diagrams
1. Maintain one direction of all blocks, from left to right or top to button. Put actors on one side
2. Avoid intersections
3. Align elements
## Making estimates
1. Latency: CPU cache is faster than RAM, RAM is faster than Disk, Disk is faster than local network, local is faster than global network
2. Throughput: see img.png
3. Capacity: see img_1.png. System design is about scaling horizontally. NoSQL we could say that the capacity is unlimited