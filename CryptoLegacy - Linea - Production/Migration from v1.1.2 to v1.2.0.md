# Migration from v1.1.2 to v1.2.0
```
Old project: QmVPvfXkFWLU6gewtQraVkmcTsTPRjU6x2Lbhh64opzKgK
New project: QmUMkLUvxdLK2daKX2PVbhEeqWCZrAGpcBdpS2WybKjgRV
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmVPvfXkFWLU6gewtQraVkmcTsTPRjU6x2Lbhh64opzKgK`)

```
docker container rm -f query_qmvpvfxkfwlu6ge && docker container rm -f node_qmvpvfxkfwlu6ge
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmvpvfxkfwlu6ge RENAME TO schema_qmumkluvxdlk2da;"

```

 3) Run new project from coordinator (`QmUMkLUvxdLK2daKX2PVbhEeqWCZrAGpcBdpS2WybKjgRV`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmvpvfxkfwlu6ge RENAME TO schema_qmumkluvxdlk2da;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
