### Start comainter

`docker-compose up -d`

### Go to the container and execute mongo command

docker exec -it \<container name\> mongo

`docker exec -it mongo_single_replica mongo`

### Initial replica set

```
rs.initiate({
  _id: "rs0",
  members: [
    {_id: 0, host: "localhost:27017"}
  ]
})
```

### Check replica set status

`rs.status()`

### Connection string

`mongodb://localhost:27017/?replicaSet=rs0`