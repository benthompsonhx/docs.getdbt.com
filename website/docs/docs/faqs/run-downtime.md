---
title: If I rerun dbt, will there be any downtime as models are rebuilt?
---
Nope! The SQL that dbt generates behind the scenes ensures that any relations are replaced atomically (i.e. your business users won't experience any downtime).

The implementation of this varies on each warehouse, check out the [logs](checking-logs) to see the SQL dbt is executing.
