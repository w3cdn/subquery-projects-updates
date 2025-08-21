# Migration from v1.0.0 to v1.1.0
```
Old project: QmUpvkmvTRkMDCGDXnAVjCBZLzZEv9UCVKHH2s3gj3hYQK
New project: QmdrqzazvSmrr6rgfxJEssJH9jqhYCZARm92UxNXMv5f86
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUpvkmvTRkMDCGDXnAVjCBZLzZEv9UCVKHH2s3gj3hYQK`)

```
docker container rm -f query_qmupvkmvtrkmdcg && docker container rm -f node_qmupvkmvtrkmdcg
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmupvkmvtrkmdcg RENAME TO schema_qmdrqzazvsmrr6r;"

```

 3) Run new project from coordinator (`QmdrqzazvSmrr6rgfxJEssJH9jqhYCZARm92UxNXMv5f86`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmupvkmvtrkmdcg RENAME TO schema_qmdrqzazvsmrr6r;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
