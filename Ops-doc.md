### Redis
* [redis-lru](https://redis.io/topics/lru-cache)
* Redis ops:
  - [Learning redis-cli article](https://redis.io/topics/rediscli)
  - ping test: (port and password is an example)
    - redis-cli -p [port] -a [password] ping
  - head of keys in redis db:
    - redis-cli -p [port] -a [password] --scan | head -10
  - monitor redis traffic:
    - redis-cli -p [port] -a [password] monitor
  - monitor redis stat for memory and connection etc:
    - redis-cli -p [port] -a [password] --stat
  - get value for key in redis db:
    - redis-cli -p [port] -a [password] GET <key>
  - get redis config for dump data and config:
    - redis-cli -p [port] -a [password] info | grep "config_file"
  - remove redis dump file:
    - delete dump files 
    - kill -9 pid
    - then redis server restart with history data
  - set config run time (try to avoid by using config file):
    - redis-cli -p * -a * config set maxmemory 2gb
  - check reids info:
    - redis-cli -p * -a * info

### Rabbit
* [rabbitmq common mistakes](https://www.cloudamqp.com/blog/2018-01-19-part4-rabbitmq-13-common-errors.html)
* [rabbitmq throughput recommendation](https://www.cloudamqp.com/blog/2018-01-08-part2-rabbitmq-best-practice-for-high-performance.html)
* [rabbitmq sharding plugin](https://github.com/rabbitmq/rabbitmq-sharding)
