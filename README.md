# Simple Redis Service
![redis up](https://user-images.githubusercontent.com/6056661/111041810-5e0b1700-844f-11eb-826e-75fc823bb8c3.png)
### Setup password
to set `Redis` password ,just put password value at
`.docker-compose/` directory as `.redis_pass_file` file, or use the sample:
```
cp .docker-compose/.redis_pass_file.local .docker-compose/.redis_pass_file
```

### Clients

Clients on the same machine, can join this service by define an external network,
for example when the client network name is `sample-network` it should define as:

```
networks:
    sample-network:
        external:
            name: redis_redis-network
```

The `external` network name, has two part, which are separated by an underline, `redis` is name of the repository, and `redis-network` is the network name of this repository
