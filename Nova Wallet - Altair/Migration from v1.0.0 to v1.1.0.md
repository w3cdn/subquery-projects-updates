# Migration from v1.0.0 to v1.1.0
```
Old project: QmPFbMgwgC9EcePX8tUjgLZ1s49PcWy3h3Rvf59bFoGndx
New project: QmPkTXq1hw1MNt8rVEySAL3izgYa5jRdQbEK9AmERhcM2S
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmPFbMgwgC9EcePX8tUjgLZ1s49PcWy3h3Rvf59bFoGndx`)

```
docker container rm -f query_qmpfbmgwgc9ecep && docker container rm -f node_qmpfbmgwgc9ecep
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmpfbmgwgc9ecep RENAME TO schema_qmpktxq1hw1mnt8;"

```

 3) Run new project from coordinator (`QmPkTXq1hw1MNt8rVEySAL3izgYa5jRdQbEK9AmERhcM2S`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmpfbmgwgc9ecep RENAME TO schema_qmpktxq1hw1mnt8;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
