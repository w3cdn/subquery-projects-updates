# Migration from v1.1.2 to v1.1.4
```
Old project: Qmc96Qkag1NuzvzAjHDrkQYHZagt7vxWL5NaZtFs6Xxz89
New project: QmVqjwMRDtbKTZFfgKa9qy7Q4qCutxNVpfLeQKBFiEJJyh
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmc96Qkag1NuzvzAjHDrkQYHZagt7vxWL5NaZtFs6Xxz89`)

```
docker container rm -f query_qmc96qkag1nuzvz && docker container rm -f node_qmc96qkag1nuzvz
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmc96qkag1nuzvz RENAME TO schema_qmvqjwmrdtbktzf;"

```

 3) Run new project from coordinator (`QmVqjwMRDtbKTZFfgKa9qy7Q4qCutxNVpfLeQKBFiEJJyh`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmc96qkag1nuzvz RENAME TO schema_qmvqjwmrdtbktzf;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
