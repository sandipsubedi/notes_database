# Sharding on MongoDB:

Great Video: https://www.youtube.com/watch?v=Rwg26U0Zs1o

- Need to Shard the database first, even though sharding happens on the collection.

### enable sharding on the database:

```js
sh.enableSharding("<database_name>")
```
- we don't have to shard collections. We can leave some not sharded.

### Checking if the collection in sharded:
```js
db.<collection_name>.getShardDistribution()
```

### Shard a collection:
- this will also create index by default:
```js
sh.shardCollection("<database_name>.<collection_name>", { "title" : "hashed" } )
//                                                            shard key
```

### To see how things are sharded on different shards:

```js
db.<collection_name>.getShardDistribution()
```

### Sharding a collection that already has some records:
- we will get an error, if things are not indexed.


create index first
```js
db.<collection_name>.createIndex( { "title": "hashed" })
```

### Check sharding status:

```js
sh.status()
```

### Different ways to shard/choose sharded key:
- Range Based key
- Hash key



