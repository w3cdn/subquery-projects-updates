# Migration from v0.9.0 to v0.9.1
```
Old project: QmQHDcqWLXoBsoaeQiN8vdSMuYSSvuUdaHa86YmKckQf4m
New project: QmcMTxW1uhNqigNhhVkpJhg78D78ZDBt3F39wp557M1mkx
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmQHDcqWLXoBsoaeQiN8vdSMuYSSvuUdaHa86YmKckQf4m`)

```
docker container rm -f query_qmqhdcqwlxobsoa && docker container rm -f node_qmqhdcqwlxobsoa
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmqhdcqwlxobsoa RENAME TO schema_qmcmtxw1uhnqign;"

```

 3) Run new project from coordinator (`QmcMTxW1uhNqigNhhVkpJhg78D78ZDBt3F39wp557M1mkx`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmqhdcqwlxobsoa RENAME TO schema_qmcmtxw1uhnqign;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
