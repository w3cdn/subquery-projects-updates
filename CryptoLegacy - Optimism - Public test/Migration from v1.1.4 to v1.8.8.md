# Migration from v1.1.4 to v1.8.8
```
Old project: QmUUsAgBHDWASkr23DGmNrEzCqPbQ1uJ9n1rTgXGG6gCfV
New project: Qmb3oR7yMEQtpPEubhjCkdiau751dGtGNN3DKTNJLkQK9W
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUUsAgBHDWASkr23DGmNrEzCqPbQ1uJ9n1rTgXGG6gCfV`)

```
docker container rm -f query_qmuusagbhdwaskr && docker container rm -f node_qmuusagbhdwaskr
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmuusagbhdwaskr RENAME TO schema_qmb3or7ymeqtppe;"

```

 3) Run new project from coordinator (`Qmb3oR7yMEQtpPEubhjCkdiau751dGtGNN3DKTNJLkQK9W`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmuusagbhdwaskr RENAME TO schema_qmb3or7ymeqtppe;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
