1. Memcached 
Is generally preferred for caching HTML fragments. Memcached is a simple key/value store. The trade-off to being simple is that it's very fast

2. Redis
Can performe many different kinds of operations on your data. It's very good for leaderboards, and keep track of unread notification data. It's very fast, but arguably not as fast as Memcached. 