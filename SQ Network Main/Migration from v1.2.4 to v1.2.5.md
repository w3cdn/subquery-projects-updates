# Migration from v1.2.4 to v1.2.5
```
Old project: QmcoJLxSeBnGwtmtNmWFCRusXVTGjYWCK1LoujthZ2NyGP
New project: QmScHyGv2fyJUB2prBKCKx3i8kGrQ3wU7USq8yBJ9DWiG9
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmcoJLxSeBnGwtmtNmWFCRusXVTGjYWCK1LoujthZ2NyGP`)

```
docker container rm -f query_qmcojlxsebngwtm && docker container rm -f node_qmcojlxsebngwtm
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmcojlxsebngwtm RENAME TO schema_qmschygv2fyjub2;"

```

 3) Run new project from coordinator (`QmScHyGv2fyJUB2prBKCKx3i8kGrQ3wU7USq8yBJ9DWiG9`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmcojlxsebngwtm RENAME TO schema_qmschygv2fyjub2;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
