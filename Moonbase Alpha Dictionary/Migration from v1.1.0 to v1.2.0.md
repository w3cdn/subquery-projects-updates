# Migration from v1.1.0 to v1.2.0
```
Old project: QmWv9Ja5AQ9cPpXb6U7sGCvkhK6XbZ7xQntTBqidsSf5SF
New project: QmcCxyskGqZBQw8LPuT619GzuqeJspjmeJPEaAuWcsTfgn
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWv9Ja5AQ9cPpXb6U7sGCvkhK6XbZ7xQntTBqidsSf5SF`)

```
docker container rm -f query_qmwv9ja5aq9cppx && docker container rm -f node_qmwv9ja5aq9cppx
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmwv9ja5aq9cppx RENAME TO schema_qmccxyskgqzbqw8;"

```

 3) Run new project from coordinator (`QmcCxyskGqZBQw8LPuT619GzuqeJspjmeJPEaAuWcsTfgn`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmwv9ja5aq9cppx RENAME TO schema_qmccxyskgqzbqw8;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
