# Migration from v1.0.0 to v1.1.0
```
Old project: QmbtSt8USCUTBWeAqevN1AwmUhKzqmtvhSdFYHYA1BviC8
New project: QmfKJuaL8iwwnSwaKt7RjTBk6Q5aUPqBzcZ1J2Q68ZvnLf
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmbtSt8USCUTBWeAqevN1AwmUhKzqmtvhSdFYHYA1BviC8`)

```
docker container rm -f query_qmbtst8uscutbwe && docker container rm -f node_qmbtst8uscutbwe
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmbtst8uscutbwe RENAME TO schema_qmfkjual8iwwnsw;"

```

 3) Run new project from coordinator (`QmfKJuaL8iwwnSwaKt7RjTBk6Q5aUPqBzcZ1J2Q68ZvnLf`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmbtst8uscutbwe RENAME TO schema_qmfkjual8iwwnsw;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
