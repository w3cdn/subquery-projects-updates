# Migration from v1.3.0 to v1.4.0
```
Old project: QmbQmLgzmoFEhAsMZDB4pGZYznXHZSHENMki1ymbDowehY
New project: QmPffAuzcstfwY6PY64bsMqDZpQV2bt5xj3zxJVubw81y8
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmbQmLgzmoFEhAsMZDB4pGZYznXHZSHENMki1ymbDowehY`)

```
docker container rm -f query_qmbqmlgzmofehas && docker container rm -f node_qmbqmlgzmofehas
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmbqmlgzmofehas RENAME TO schema_qmpffauzcstfwy6;"

```

 3) Run new project from coordinator (`QmPffAuzcstfwY6PY64bsMqDZpQV2bt5xj3zxJVubw81y8`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmbqmlgzmofehas RENAME TO schema_qmpffauzcstfwy6;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
