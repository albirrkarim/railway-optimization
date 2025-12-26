# Railway Optimization

Reduce your memory usage by 90%

# WordPress
```
PHP_MEMORY_LIMIT="128M"
PHP_INI_MEMORY_LIMIT="128M"
```

# Maria DB

```
MYSQL_INNODB_BUFFER_POOL_SIZE="128M"
MYSQL_INNODB_LOG_BUFFER_SIZE="16M"
MYSQL_MAX_CONNECTIONS="50"
MYSQL_THREAD_CACHE_SIZE="16"
MYSQL_TABLE_OPEN_CACHE="400"
MYSQL_PERFORMANCE_SCHEMA="0"
```

# Postgres
```
PGOPTIONS="-c shared_buffers=128MB -c work_mem=4MB -c maintenance_work_mem=32MB -c effective_cache_size=256MB -c max_connections=15"
```

# N8N

```
N8N_LOG_LEVEL="error"
EXECUTIONS_DATA_SAVE_ON_SUCCESS="false"
QUEUE_BULL_LOG_LEVEL="error"
EXECUTIONS_PROCESS="queue"
EXECUTIONS_DATA_PRUNE="true"
EXECUTIONS_DATA_PRUNE_MAXAGE="24"
NODE_OPTIONS="--max-old-space-size=256"
N8N_WORKER_THREADS="1"
```
