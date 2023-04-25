## Caching
1. Pros: Improve read performance, reduce the load (throughput)
2. Cons: Increases complexity, consumes resources

## Caching Strategies
1. Cache aside (most common, app has access to both Cache and Storage, Redis like): pros: cache only what's needed, cons: cache misses are expensive, data staleness, complex to implement, see img.png 
2. Read through: app reads from cache only, common in ORM frameworks, pros: cache only what's needed, transparent. cons: cache misses are expensive, data staleness, reliability. see img_1.png
3. Write through: write to cache then the storage. pros: up-to-date data. cons: writes are expensive, redundant data. see img_2.png
4. Write behind: write doesn't write to the storage immediately , it waits for more writes or the timeout then writes to the storage. pros: no write penalty, reduced load on storage. cons: reliability and lack of consistency. see img_3.png. If the cache crashes we loose some data

## Eviction Policies
1. LRU: mostly default, based on the linked list, head item is the next item to be removed. When there is a cache hit it gets moved to the tail. If there is a cache miss it gets put to the tail and pushes one el out (the head). False cache eviction problem if a lot of new keys are requested at once it may evict some popular
2. LFU: solves LRU problems, more complicated to implement. Every key has a counter and when there is a hit the counter for that key is reset, where there is a miss the key with a largest counter will be evicted. Overhead of counter hits per key.

## Redis
In memory key-value store, limited by RAM per node. High throughput, 100K+ reqs/sec/node. Supports TTL, persistence but can lose recent data