# Migration from v1.2.8 to v1.2.9
```
Old project: QmNfHk9n4KPJJkiJ2WA4hjd3Zpk6d2tR52WeFEtxqgK6Ck
New project: QmQbSumWfjgEfrPGsnNGAhq7SyXDjxKQCXLSjRiPpgFktd
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmNfHk9n4KPJJkiJ2WA4hjd3Zpk6d2tR52WeFEtxqgK6Ck`)

```
docker container rm -f query_qmnfhk9n4kpjjki && docker container rm -f node_qmnfhk9n4kpjjki
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmnfhk9n4kpjjki RENAME TO schema_qmqbsumwfjgefrp;"

```

 3) Run new project from coordinator (`QmQbSumWfjgEfrPGsnNGAhq7SyXDjxKQCXLSjRiPpgFktd`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmnfhk9n4kpjjki RENAME TO schema_qmqbsumwfjgefrp;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
