### 1. Drop all tables postgress.

```
DROP SCHEMA public CASCADE;
CREATE SCHEMA public;
```

### 2. Docker last 50 logs
```
docker logs --tail 50 --follow --timestamps <container_id>
```

### 3. Enter into container
```
docker exec -it <container_id> /bin/bash
```
### 4. Accessing through ssh
```
ssh root@<im_address> -p <port>
```
### 5. Creating backup from postgres database:
```
pg_dump -h <host> -p <port> -U <username> -Fc <database_name> > <Name_you_want_to_keep_that_file.dump>

```
### 6. Coping data into postgres container:
```
docker cp <dump_file> container_id:/
```

### 7. Restoring backup database data
```
pg_restore --no-owner --no-privileges --role=postgres -U <user_name> -d <database_name> -1 <dump_file>
```
### 8. Take input output from file
```
freopen("input.txt", "r", stdin);
freopen("output.txt", "w", stdout);
```
