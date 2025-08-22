# Migration from v1.3.0 to v1.3.1
```
Old project: QmWpEu3L6CivgQAj8LR3d5ZVsfEYVs7zeR9ju4YNEo7HPy
New project: QmRzvBkdKn9AXyQxAMobZa7EKdP6U3p8RZc7JGwAWs478z
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWpEu3L6CivgQAj8LR3d5ZVsfEYVs7zeR9ju4YNEo7HPy`)

```
docker container rm -f query_qmwpeu3l6civgqa && docker container rm -f node_qmwpeu3l6civgqa
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmwpeu3l6civgqa RENAME TO schema_qmrzvbkdkn9axyq;"

```

 3) Run new project from coordinator (`QmRzvBkdKn9AXyQxAMobZa7EKdP6U3p8RZc7JGwAWs478z`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmwpeu3l6civgqa RENAME TO schema_qmrzvbkdkn9axyq;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
