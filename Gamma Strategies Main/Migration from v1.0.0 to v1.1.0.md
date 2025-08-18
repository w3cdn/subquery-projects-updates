# Migration from v1.0.0 to v1.1.0
```
Old project: QmaowWuJ8E9hibSUfrhtKdhCBkwxhRzrcrvw8DQNcEBiQx
New project: QmXbC4pnjrxpmoGW76jPmjaBJs1nV1DYkAJStMVrxewZW6
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmaowWuJ8E9hibSUfrhtKdhCBkwxhRzrcrvw8DQNcEBiQx`)

```
docker container rm -f query_qmaowwuj8e9hibs && docker container rm -f node_qmaowwuj8e9hibs
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmaowwuj8e9hibs RENAME TO schema_qmxbc4pnjrxpmog;"

```

 3) Run new project from coordinator (`QmXbC4pnjrxpmoGW76jPmjaBJs1nV1DYkAJStMVrxewZW6`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmaowwuj8e9hibs RENAME TO schema_qmxbc4pnjrxpmog;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
