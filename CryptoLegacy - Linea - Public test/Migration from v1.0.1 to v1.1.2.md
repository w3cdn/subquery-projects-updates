# Migration from v1.0.1 to v1.1.2
```
Old project: Qme625bmRd35K7T2efLid4CoUHY3ifK7i51uq6ZpBYjT6D
New project: Qmc96Qkag1NuzvzAjHDrkQYHZagt7vxWL5NaZtFs6Xxz89
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qme625bmRd35K7T2efLid4CoUHY3ifK7i51uq6ZpBYjT6D`)

```
docker container rm -f query_qme625bmrd35k7t && docker container rm -f node_qme625bmrd35k7t
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qme625bmrd35k7t RENAME TO schema_qmc96qkag1nuzvz;"

```

 3) Run new project from coordinator (`Qmc96Qkag1NuzvzAjHDrkQYHZagt7vxWL5NaZtFs6Xxz89`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qme625bmrd35k7t RENAME TO schema_qmc96qkag1nuzvz;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
