# Migration from v1.0.0 to v1.1.0
```
Old project: QmPo8kuJUYjM4LEdTkVmPWuW6doP2BusY2BLy9vxKgLpG9
New project: QmR5tfCMAoD162BpR1DxqvtZue5rQPQrMGqSHc4SsWS2ap
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmPo8kuJUYjM4LEdTkVmPWuW6doP2BusY2BLy9vxKgLpG9`)

```
docker container rm -f query_qmpo8kujuyjm4le && docker container rm -f node_qmpo8kujuyjm4le
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmpo8kujuyjm4le RENAME TO schema_qmr5tfcmaod162b;"

```

 3) Run new project from coordinator (`QmR5tfCMAoD162BpR1DxqvtZue5rQPQrMGqSHc4SsWS2ap`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmpo8kujuyjm4le RENAME TO schema_qmr5tfcmaod162b;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
