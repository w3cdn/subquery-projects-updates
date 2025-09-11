# Migration from v1.1.4 to v1.8.8
```
Old project: QmVqjwMRDtbKTZFfgKa9qy7Q4qCutxNVpfLeQKBFiEJJyh
New project: QmP7YCVTzS99XRSAkoo8aiosAWjrqj7BpgSm71DYWgaVJQ
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmVqjwMRDtbKTZFfgKa9qy7Q4qCutxNVpfLeQKBFiEJJyh`)

```
docker container rm -f query_qmvqjwmrdtbktzf && docker container rm -f node_qmvqjwmrdtbktzf
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmvqjwmrdtbktzf RENAME TO schema_qmp7ycvtzs99xrs;"

```

 3) Run new project from coordinator (`QmP7YCVTzS99XRSAkoo8aiosAWjrqj7BpgSm71DYWgaVJQ`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmvqjwmrdtbktzf RENAME TO schema_qmp7ycvtzs99xrs;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
