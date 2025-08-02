# Migration from v1.1.2 to v1.2.0
```
Old project: QmTwxiDWAakXDuvAqYfcrbffupTRLoRbgiCszzf41iM9JY
New project: QmZWKFTpgnfeq6toPGEAz52s8FX4mA3pgdzy3Lrj6ihHbW
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmTwxiDWAakXDuvAqYfcrbffupTRLoRbgiCszzf41iM9JY`)

```
docker container rm -f query_qmtwxidwaakxduv && docker container rm -f node_qmtwxidwaakxduv
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmtwxidwaakxduv RENAME TO schema_qmzwkftpgnfeq6t;"

```

 3) Run new project from coordinator (`QmZWKFTpgnfeq6toPGEAz52s8FX4mA3pgdzy3Lrj6ihHbW`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmtwxidwaakxduv RENAME TO schema_qmzwkftpgnfeq6t;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
