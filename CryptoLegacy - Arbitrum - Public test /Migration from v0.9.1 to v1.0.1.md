# Migration from v0.9.1 to v1.0.1
```
Old project: QmcMTxW1uhNqigNhhVkpJhg78D78ZDBt3F39wp557M1mkx
New project: QmZ5iXBtKyrEGQ5nbYje3SjvTDHobuzYp23TzaPZRnhcxG
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmcMTxW1uhNqigNhhVkpJhg78D78ZDBt3F39wp557M1mkx`)

```
docker container rm -f query_qmcmtxw1uhnqign && docker container rm -f node_qmcmtxw1uhnqign
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmcmtxw1uhnqign RENAME TO schema_qmz5ixbtkyregq5;"

```

 3) Run new project from coordinator (`QmZ5iXBtKyrEGQ5nbYje3SjvTDHobuzYp23TzaPZRnhcxG`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmcmtxw1uhnqign RENAME TO schema_qmz5ixbtkyregq5;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
