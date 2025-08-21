# Migration from v1.2.0 to v1.3.0
```
Old project: QmSCNvH1dPT8AwSMbxbePDe5QNMVre81wHfXgA9MwLrFWF
New project: QmbQmLgzmoFEhAsMZDB4pGZYznXHZSHENMki1ymbDowehY
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmSCNvH1dPT8AwSMbxbePDe5QNMVre81wHfXgA9MwLrFWF`)

```
docker container rm -f query_qmscnvh1dpt8aws && docker container rm -f node_qmscnvh1dpt8aws
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmscnvh1dpt8aws RENAME TO schema_qmbqmlgzmofehas;"

```

 3) Run new project from coordinator (`QmbQmLgzmoFEhAsMZDB4pGZYznXHZSHENMki1ymbDowehY`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmscnvh1dpt8aws RENAME TO schema_qmbqmlgzmofehas;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
