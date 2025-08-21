# Migration from v1.1.0 to v1.2.0
```
Old project: Qmbe5g5vbEJYYAfpjcwNDzuhjeyaEQPQbxKyKx6PveYnR8
New project: QmVuW3RxNLySTXzv2mA3xknT7ndXzRWAYHkJ86biYqLUs1
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmbe5g5vbEJYYAfpjcwNDzuhjeyaEQPQbxKyKx6PveYnR8`)

```
docker container rm -f query_qmbe5g5vbejyyaf && docker container rm -f node_qmbe5g5vbejyyaf
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmbe5g5vbejyyaf RENAME TO schema_qmvuw3rxnlystxz;"

```

 3) Run new project from coordinator (`QmVuW3RxNLySTXzv2mA3xknT7ndXzRWAYHkJ86biYqLUs1`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmbe5g5vbejyyaf RENAME TO schema_qmvuw3rxnlystxz;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
