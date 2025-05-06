# Migration from v1.2.9 to v1.3.0
```
Old project: QmQbSumWfjgEfrPGsnNGAhq7SyXDjxKQCXLSjRiPpgFktd
New project: QmQqqmwwaBben8ncfHo3DMnDxyWFk5QcEdTmbevzKj7DBd
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmQbSumWfjgEfrPGsnNGAhq7SyXDjxKQCXLSjRiPpgFktd`)

```
docker container rm -f query_qmqbsumwfjgefrp && docker container rm -f node_qmqbsumwfjgefrp
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmqbsumwfjgefrp RENAME TO schema_qmqqqmwwabben8n;"

```

 3) Run new project from coordinator (`QmQqqmwwaBben8ncfHo3DMnDxyWFk5QcEdTmbevzKj7DBd`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmqbsumwfjgefrp RENAME TO schema_qmqqqmwwabben8n;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
