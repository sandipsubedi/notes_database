# Redis CLI:

### To open Redis CLI:

```ruby
redis-cli
```

### To Set:

```ruby
127.0.0.1:6379> set "name" "hello world"
OK
```

### To get:

```ruby
127.0.0.1:6379> get "name"
"hello world"
```

### To delete:

```ruby
127.0.0.1:6379> del "name"
(integer) 1
127.0.0.1:6379> get "name"
(nil)
127.0.0.1:6379>
```

### To delete multiple:

```ruby
127.0.0.1:6379> del "name1" "name1"
(integer) 2
```

### To get all the keys:

```ruby
redis-cli keys "*"
```



