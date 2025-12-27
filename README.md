# Railway Optimization

Reduce your memory usage by 90%. Try free trial on first month using this link https://railway.com?referralCode=Dx-qfW

# WordPress

ENV variable
```
PHP_MEMORY_LIMIT="128M"
PHP_INI_MEMORY_LIMIT="128M"
```

# Maria DB

ENV variable
```
MYSQL_INNODB_BUFFER_POOL_SIZE="64M"
MYSQL_INNODB_LOG_BUFFER_SIZE="8M"
MYSQL_MAX_CONNECTIONS="10"
MYSQL_THREAD_CACHE_SIZE="4"
MYSQL_TABLE_OPEN_CACHE="200"
MYSQL_PERFORMANCE_SCHEMA="0"
```

# Postgres

ENV variable
```
PGOPTIONS="-c shared_buffers=128MB -c work_mem=4MB -c maintenance_work_mem=32MB -c effective_cache_size=256MB -c max_connections=15"
```

# N8N

<img width="921" height="673" alt="Screenshot 2025-12-26 at 18 11 30" src="https://github.com/user-attachments/assets/37166063-4878-43bc-b26e-f9c602e22a02" />

n8n + sql lite
https://railway.com/deploy/n8n-cheapest-to-run

Export import
```
n8n export:workflow --backup --output=/root/.n8n/tmp/workflows
n8n export:credentials --backup --output=/root/.n8n/tmp/credentials

n8n import:credentials --separate --input=/root/.n8n/tmp/credentials
n8n import:workflow --separate --input=/root/.n8n/tmp/workflows
```

ENV variable
```
EXECUTIONS_DATA_SAVE_ON_SUCCESS="false"
QUEUE_BULL_LOG_LEVEL="error"
EXECUTIONS_PROCESS="queue"
EXECUTIONS_DATA_PRUNE="true"
EXECUTIONS_DATA_PRUNE_MAXAGE="24"

NODE_OPTIONS="--max-old-space-size=256"

N8N_LOG_LEVEL="error"
N8N_DEFAULT_BINARY_DATA_MODE=filesystem
N8N_WORKER_THREADS="1"
```

Download credentials.json and workflows.json into local computer

```
railway ssh \
  --project=xx \
  --environment=xx \
  --service=xxx \
  -- cat /root/.n8n/workflows.json \
> workflows.json
```


