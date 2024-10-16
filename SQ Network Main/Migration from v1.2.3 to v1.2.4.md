# Migration from v1.2.3 to v1.2.4
```
Old project: QmULvX7eUVbyBzPqFJs1A8udTRMtkUZWjYK5BZD5hMztMt
New project: QmcoJLxSeBnGwtmtNmWFCRusXVTGjYWCK1LoujthZ2NyGP
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmULvX7eUVbyBzPqFJs1A8udTRMtkUZWjYK5BZD5hMztMt`)

```
docker container rm -f query_qmulvx7euvbybzp && docker container rm -f node_qmulvx7euvbybzp
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmulvx7euvbybzp RENAME TO schema_qmcojlxsebngwtm;"

```

 3) Run new project from coordinator (`QmcoJLxSeBnGwtmtNmWFCRusXVTGjYWCK1LoujthZ2NyGP`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmulvx7euvbybzp RENAME TO schema_qmcojlxsebngwtm;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
