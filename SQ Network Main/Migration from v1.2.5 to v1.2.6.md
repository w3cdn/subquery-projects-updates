# Migration from v1.2.5 to v1.2.6
```
Old project: QmScHyGv2fyJUB2prBKCKx3i8kGrQ3wU7USq8yBJ9DWiG9
New project: QmVnojxfmZJzWihvmSuixZsAxPrGqVeNB4EdTtmL3UGiFY
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmScHyGv2fyJUB2prBKCKx3i8kGrQ3wU7USq8yBJ9DWiG9`)

```
docker container rm -f query_qmschygv2fyjub2 && docker container rm -f node_qmschygv2fyjub2
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmschygv2fyjub2 RENAME TO schema_qmvnojxfmzjzwih;"

```

 3) Run new project from coordinator (`QmVnojxfmZJzWihvmSuixZsAxPrGqVeNB4EdTtmL3UGiFY`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmschygv2fyjub2 RENAME TO schema_qmvnojxfmzjzwih;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
