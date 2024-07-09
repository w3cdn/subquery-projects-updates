# Migration from v1.0.0 to v1.1.0
```
Old project: QmRonzFGNrsmpG2NrVhcVC6rCtCBqYFupX6MEECReWXWZT
New project: QmWD7SwH7aUyVvyydZRzS7XtM8bSU6izkvWgzYgrtw3V82
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmRonzFGNrsmpG2NrVhcVC6rCtCBqYFupX6MEECReWXWZT`)

```
docker container rm -f query_qmronzfgnrsmpg2 && docker container rm -f node_qmronzfgnrsmpg2
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmronzfgnrsmpg2 RENAME TO schema_qmwd7swh7auyvvy;"

```

 3) Run new project from coordinator (`QmWD7SwH7aUyVvyydZRzS7XtM8bSU6izkvWgzYgrtw3V82`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmronzfgnrsmpg2 RENAME TO schema_qmwd7swh7auyvvy;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
