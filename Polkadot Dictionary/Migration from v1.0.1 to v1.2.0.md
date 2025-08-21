# Migration from v1.0.1 to v1.2.0
```
Old project: QmUGBdhQKnzE8q6x6MPqP6LNZGa8gzXf5gkdmhzWjdFGfL
New project: QmSxAgGGpaMrYzooWpydmwzutREwomL5nupLZqxURzuJTo
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUGBdhQKnzE8q6x6MPqP6LNZGa8gzXf5gkdmhzWjdFGfL`)

```
docker container rm -f query_qmugbdhqknze8q6 && docker container rm -f node_qmugbdhqknze8q6
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmugbdhqknze8q6 RENAME TO schema_qmsxagggpamryzo;"

```

 3) Run new project from coordinator (`QmSxAgGGpaMrYzooWpydmwzutREwomL5nupLZqxURzuJTo`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmugbdhqknze8q6 RENAME TO schema_qmsxagggpamryzo;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
