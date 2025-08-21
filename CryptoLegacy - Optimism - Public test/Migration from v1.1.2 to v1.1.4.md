# Migration from v1.1.2 to v1.1.4
```
Old project: Qmbpcmu5FBjXDvUBJ8BNEddqz31dLWsqp42QQ66Vt1SEGD
New project: QmUUsAgBHDWASkr23DGmNrEzCqPbQ1uJ9n1rTgXGG6gCfV
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmbpcmu5FBjXDvUBJ8BNEddqz31dLWsqp42QQ66Vt1SEGD`)

```
docker container rm -f query_qmbpcmu5fbjxdvu && docker container rm -f node_qmbpcmu5fbjxdvu
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmbpcmu5fbjxdvu RENAME TO schema_qmuusagbhdwaskr;"

```

 3) Run new project from coordinator (`QmUUsAgBHDWASkr23DGmNrEzCqPbQ1uJ9n1rTgXGG6gCfV`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmbpcmu5fbjxdvu RENAME TO schema_qmuusagbhdwaskr;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
