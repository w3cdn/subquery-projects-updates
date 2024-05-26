# Migration from v1.0.0 to v1.1.0
```
Old project: QmUgn2eP1nvAECSe9HE9zTHTHwkQMDwSN7rpB1aXcsthfe
New project: QmWv9Ja5AQ9cPpXb6U7sGCvkhK6XbZ7xQntTBqidsSf5SF
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUgn2eP1nvAECSe9HE9zTHTHwkQMDwSN7rpB1aXcsthfe`)

```
docker container rm -f query_qmugn2ep1nvaecs && docker container rm -f node_qmugn2ep1nvaecs
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmugn2ep1nvaecs RENAME TO schema_qmwv9ja5aq9cppx;"

```

 3) Run new project from coordinator (`QmWv9Ja5AQ9cPpXb6U7sGCvkhK6XbZ7xQntTBqidsSf5SF`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmugn2ep1nvaecs RENAME TO schema_qmwv9ja5aq9cppx;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
