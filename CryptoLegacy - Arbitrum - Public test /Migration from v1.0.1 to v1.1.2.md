# Migration from v1.0.1 to v1.1.2
```
Old project: QmZ5iXBtKyrEGQ5nbYje3SjvTDHobuzYp23TzaPZRnhcxG
New project: QmfWNqomCM2VRRGST2XeZzAPwitBy2zu66UMP3AUcMeCsF
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZ5iXBtKyrEGQ5nbYje3SjvTDHobuzYp23TzaPZRnhcxG`)

```
docker container rm -f query_qmz5ixbtkyregq5 && docker container rm -f node_qmz5ixbtkyregq5
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmz5ixbtkyregq5 RENAME TO schema_qmfwnqomcm2vrrg;"

```

 3) Run new project from coordinator (`QmfWNqomCM2VRRGST2XeZzAPwitBy2zu66UMP3AUcMeCsF`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmz5ixbtkyregq5 RENAME TO schema_qmfwnqomcm2vrrg;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
