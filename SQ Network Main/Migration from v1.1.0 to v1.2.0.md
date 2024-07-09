# Migration from v1.1.0 to v1.2.0
```
Old project: QmZdLhKt44hmW56YS63rwr1NbkyGuG224oHjFypeXUiahW
New project: QmUQy6VqsLgKNGyRrrKQdMnwGdvFD2nfgEKeTJq8G4oqAB
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZdLhKt44hmW56YS63rwr1NbkyGuG224oHjFypeXUiahW`)

```
docker container rm -f query_qmzdlhkt44hmw56 && docker container rm -f node_qmzdlhkt44hmw56
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmzdlhkt44hmw56 RENAME TO schema_qmuqy6vqslgkngy;"

```

 3) Run new project from coordinator (`QmUQy6VqsLgKNGyRrrKQdMnwGdvFD2nfgEKeTJq8G4oqAB`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmzdlhkt44hmw56 RENAME TO schema_qmuqy6vqslgkngy;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
