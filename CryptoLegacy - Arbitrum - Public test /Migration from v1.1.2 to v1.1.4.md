# Migration from v1.1.2 to v1.1.4
```
Old project: QmfWNqomCM2VRRGST2XeZzAPwitBy2zu66UMP3AUcMeCsF
New project: QmX2SWngardD75TP99ixP8NucR6V7QvZi7a7i3ABhx5WVu
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmfWNqomCM2VRRGST2XeZzAPwitBy2zu66UMP3AUcMeCsF`)

```
docker container rm -f query_qmfwnqomcm2vrrg && docker container rm -f node_qmfwnqomcm2vrrg
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmfwnqomcm2vrrg RENAME TO schema_qmx2swngardd75t;"

```

 3) Run new project from coordinator (`QmX2SWngardD75TP99ixP8NucR6V7QvZi7a7i3ABhx5WVu`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmfwnqomcm2vrrg RENAME TO schema_qmx2swngardd75t;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
