# Migration from v1.2.0 to v1.3.0
```
Old project: QmajkFFn6eRmtSTUFGGec51ivFibMvKsa8vzMBvsvkPAxs
New project: QmWpEu3L6CivgQAj8LR3d5ZVsfEYVs7zeR9ju4YNEo7HPy
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmajkFFn6eRmtSTUFGGec51ivFibMvKsa8vzMBvsvkPAxs`)

```
docker container rm -f query_qmajkffn6ermtst && docker container rm -f node_qmajkffn6ermtst
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmajkffn6ermtst RENAME TO schema_qmwpeu3l6civgqa;"

```

 3) Run new project from coordinator (`QmWpEu3L6CivgQAj8LR3d5ZVsfEYVs7zeR9ju4YNEo7HPy`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmajkffn6ermtst RENAME TO schema_qmwpeu3l6civgqa;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
