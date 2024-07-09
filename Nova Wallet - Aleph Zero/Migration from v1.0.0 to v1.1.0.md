# Migration from v1.0.0 to v1.1.0
```
Old project: QmZNNYQqBs3c9f3t7UUybt1Unr49F5gTEdvU3Byv6DntKo
New project: QmeMyqVHN7YxCHT6ftpaJ26APMCAPi4VfV5T1Zj8o8Cy3c
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZNNYQqBs3c9f3t7UUybt1Unr49F5gTEdvU3Byv6DntKo`)

```
docker container rm -f query_qmznnyqqbs3c9f3 && docker container rm -f node_qmznnyqqbs3c9f3
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmznnyqqbs3c9f3 RENAME TO schema_qmemyqvhn7yxcht;"

```

 3) Run new project from coordinator (`QmeMyqVHN7YxCHT6ftpaJ26APMCAPi4VfV5T1Zj8o8Cy3c`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmznnyqqbs3c9f3 RENAME TO schema_qmemyqvhn7yxcht;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
