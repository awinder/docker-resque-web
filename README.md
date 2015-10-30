# docker-resque-web

A docker image with command-line options for specifying your redis instance(s).  Supports redis sentinel as well as single redis hosts.

### Usage

Specifying Sentinel nodes:

```
docker run -p 9292:9292 awinder/resque-web --sentinel sentinel1:26379 --sentinel sentinel1:26379 --master mymaster
```

Specifying a single Redis node:

```
docker run -p 9292:9292 awinder/resque-web --redis redis.my.host
```

Specifying a single Redis node and a database number:

```
docker run -p 9292:9292 awinder/resque-web --redis redis.my.host --db 3
```
