# Migration from v1.1.3 to v1.2.0
```
Old project: QmUm1ixPA9g5zuoSJiAjSNthVurnX8ytELjz2FYBdQdk3D
New project: QmPJEmGgCKeB2aeygz5RLH1c99fLH4CtJQj4amUUhhPE56
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUm1ixPA9g5zuoSJiAjSNthVurnX8ytELjz2FYBdQdk3D`)

```
docker container rm -f query_qmum1ixpa9g5zuo && docker container rm -f node_qmum1ixpa9g5zuo
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmum1ixpa9g5zuo RENAME TO schema_qmpjemggckeb2ae;"

```

 3) Run new project from coordinator (`QmPJEmGgCKeB2aeygz5RLH1c99fLH4CtJQj4amUUhhPE56`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmum1ixpa9g5zuo RENAME TO schema_qmpjemggckeb2ae;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
