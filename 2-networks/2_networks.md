## Load Balancing
1. Is a machine that runs a reversed proxy, runs in pairs.
2. Goal is to distribute requests between multiple servers
3. Strategies: Round robin, Least connections, Resource based, Wighted variants of those on the left, Random
4. Types of LBs: Layer4 based on the Transport Layer and has access to TCP or UDP, IP and Port. Layer7 on the Application Layer, can access to everything from Layer4 plus HTTP headers, cookies and payload
5. Some of the open source LBs: Nginx, HAProxy, Traefik
6. Main benefits: Resilience (if one node fails will reroute the next req to the other server), Scalability (makes system scalable - horizontal scaling)
7. Usually LBs are in front of every service

## CDN
1. Content Delivery Network - put a static content on the CDN servers across the globe, a cache for the static assets close to the users (images, CSS, HTML, JS)
2. Types: Push (a new log is automatically uploaded to all CDN servers, human initiate the process), not for huge content. Pull: if there are no asset in CDN when is requested it gets uploaded to the CDN, for huge amount of assets  
3. Summery: see img.png