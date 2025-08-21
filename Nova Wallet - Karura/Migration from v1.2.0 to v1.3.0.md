# Migration from v1.2.0 to v1.3.0
```
Old project: QmfALL4KNfwUdCr1EUDrioDuFFN5CmGrunrpHy4iVMg2dR
New project: QmUAo3KNUiKpLwZXoygCF5cFLFxBoNbwWYJmhwQba672Dn
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmfALL4KNfwUdCr1EUDrioDuFFN5CmGrunrpHy4iVMg2dR`)

```
docker container rm -f query_qmfall4knfwudcr && docker container rm -f node_qmfall4knfwudcr
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmfall4knfwudcr RENAME TO schema_qmuao3knuikplwz;"

```

 3) Run new project from coordinator (`QmUAo3KNUiKpLwZXoygCF5cFLFxBoNbwWYJmhwQba672Dn`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmfall4knfwudcr RENAME TO schema_qmuao3knuikplwz;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
