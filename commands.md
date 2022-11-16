### 1. Drop all tables postgress.

```
DROP SCHEMA public CASCADE;
CREATE SCHEMA public;
```

### 2. Docker last 50 logs
```
docker logs --tail 50 --follow --timestamps 15b1c3
```
