# Migration from v1.2.6 to v1.2.7
```
Old project: QmVnojxfmZJzWihvmSuixZsAxPrGqVeNB4EdTtmL3UGiFY
New project: QmWaV7Be6KwdhU6v6tUaVCyb1R3rUxYX987fGNJkQ4QisU
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmVnojxfmZJzWihvmSuixZsAxPrGqVeNB4EdTtmL3UGiFY`)

```
docker container rm -f query_qmvnojxfmzjzwih && docker container rm -f node_qmvnojxfmzjzwih
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmvnojxfmzjzwih RENAME TO schema_qmwav7be6kwdhu6;"

```

 3) Run new project from coordinator (`QmWaV7Be6KwdhU6v6tUaVCyb1R3rUxYX987fGNJkQ4QisU`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmvnojxfmzjzwih RENAME TO schema_qmwav7be6kwdhu6;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
