# Migration from v1.0.0 to v1.1.0
```
Old project: QmUgn2eP1nvAECSe9HE9zTHTHwkQMDwSN7rpB1aXcsthfe
New project: QmWv9Ja5AQ9cPpXb6U7sGCvkhK6XbZ7xQntTBqidsSf5SF
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUgn2eP1nvAECSe9HE9zTHTHwkQMDwSN7rpB1aXcsthfe`)
```
docker container rm -f query_qmugn2ep1nvaecsdocker container rm -f node_qmugn2ep1nvaecs```
 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmugn2ep1nvaecs RENAME TO schema_qmwv9ja5aq9cppx;"
```
 3) Run new project from coordinator (`QmWv9Ja5AQ9cPpXb6U7sGCvkhK6XbZ7xQntTBqidsSf5SF`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmugn2ep1nvaecs RENAME TO schema_qmwv9ja5aq9cppx;`
