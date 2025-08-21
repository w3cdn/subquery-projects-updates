# Migration from v1.0.0 to v1.1.0
```
Old project: QmXb1uHC673iHM2DLuxWRRn28W9Gevb6WkMHpkXwzPC9sW
New project: QmPwGk3PBAmSra1vWriD5Hb3ZKZcGmP2xhCubVgw8JZ5y8
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmXb1uHC673iHM2DLuxWRRn28W9Gevb6WkMHpkXwzPC9sW`)

```
docker container rm -f query_qmxb1uhc673ihm2 && docker container rm -f node_qmxb1uhc673ihm2
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmxb1uhc673ihm2 RENAME TO schema_qmpwgk3pbamsra1;"

```

 3) Run new project from coordinator (`QmPwGk3PBAmSra1vWriD5Hb3ZKZcGmP2xhCubVgw8JZ5y8`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmxb1uhc673ihm2 RENAME TO schema_qmpwgk3pbamsra1;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
