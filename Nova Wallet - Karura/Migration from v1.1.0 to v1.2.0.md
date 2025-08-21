# Migration from v1.1.0 to v1.2.0
```
Old project: QmS4azuhvLmCfjRs4ZA5qK9QTCi4TGPqVoQWc9oF6MGSjJ
New project: QmfALL4KNfwUdCr1EUDrioDuFFN5CmGrunrpHy4iVMg2dR
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmS4azuhvLmCfjRs4ZA5qK9QTCi4TGPqVoQWc9oF6MGSjJ`)

```
docker container rm -f query_qms4azuhvlmcfjr && docker container rm -f node_qms4azuhvlmcfjr
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qms4azuhvlmcfjr RENAME TO schema_qmfall4knfwudcr;"

```

 3) Run new project from coordinator (`QmfALL4KNfwUdCr1EUDrioDuFFN5CmGrunrpHy4iVMg2dR`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qms4azuhvlmcfjr RENAME TO schema_qmfall4knfwudcr;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
