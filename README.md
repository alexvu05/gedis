# A multi-threaded Redis-like server

## How to run

```
  cd cmd
  go run main.go
  # on another terminal
  redis-cli -p 3000
```

## Supported features

- Server Models:
  - Simple TCP Server
  - Thread pool
  - One thread per connection model
  - Multiplexing
  - Shared-nothing architecture
- [RESP protocol](https://redis.io/docs/latest/develop/reference/protocol-spec)
- Commands:
  - [Hashtable](https://redis.io/docs/latest/develop/data-types/hashes): GET, SET, DEL, TTL
  - [Simple Set](https://redis.io/docs/latest/develop/data-types/sets): SADD, SREM, SMEMEBERS, SISMEMBER
  - [Sorted Set](https://redis.io/docs/latest/develop/data-types/sorted-sets): ZADD, ZSCORE, ZRANK
  - [Count-min sketch](https://redis.io/docs/latest/develop/data-types/probabilistic/count-min-sketch): CMS.INITBYDIM, CMS.INCRBY, CMS.QUERY
  - [Bloom Filter](https://redis.io/docs/latest/develop/data-types/probabilistic/bloom-filter): BF.RESERVE, BF.MADD, BF.EXISTS
- Passive, Active expired key deletion
- Cache eviction: random, approximated LRU
- Graceful shutdown

## Todo

- More commands:
  - [Geospatial](https://redis.io/docs/latest/develop/data-types/geospatial)
  - List
  - Bitmap
  - Hyperloglog
  - Queue
- [Pipeline](https://redis.io/docs/latest/develop/using-commands/pipelining)
- Authentication
- Data persistence: RDB, AOF
  ...