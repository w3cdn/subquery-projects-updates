# Migration from v1.1.0 to v1.2.0
```
Old project: QmWm7SG64PwYsX5vhmuLbrZ4issMMBVPNFoJSusudDVPzf
New project: QmSCNvH1dPT8AwSMbxbePDe5QNMVre81wHfXgA9MwLrFWF
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWm7SG64PwYsX5vhmuLbrZ4issMMBVPNFoJSusudDVPzf`)

```
docker container rm -f query_qmwm7sg64pwysx5 && docker container rm -f node_qmwm7sg64pwysx5
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmwm7sg64pwysx5 RENAME TO schema_qmscnvh1dpt8aws;"

```

 3) Run new project from coordinator (`QmSCNvH1dPT8AwSMbxbePDe5QNMVre81wHfXgA9MwLrFWF`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmwm7sg64pwysx5 RENAME TO schema_qmscnvh1dpt8aws;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
