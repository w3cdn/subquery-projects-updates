# Migration from v1.0.0 to v1.1.0
```
Old project: Qma6BeSQGHrhP5aydmkQcJCR25TEwuNMogS5boovBBwoeW
New project: QmP1BMJoyJ5iFq6XLSfTJ3D23iWuTG1tnsEffJpNieQnwN
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qma6BeSQGHrhP5aydmkQcJCR25TEwuNMogS5boovBBwoeW`)

```
docker container rm -f query_qma6besqghrhp5a && docker container rm -f node_qma6besqghrhp5a
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qma6besqghrhp5a RENAME TO schema_qmp1bmjoyj5ifq6;"

```

 3) Run new project from coordinator (`QmP1BMJoyJ5iFq6XLSfTJ3D23iWuTG1tnsEffJpNieQnwN`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qma6besqghrhp5a RENAME TO schema_qmp1bmjoyj5ifq6;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)