# Migration from v1.1.2 to v1.1.4
```
Old project: QmVfe9eFWTRbEmpKP7ySrSVf9xuZKB1e8ToVM8ECNDCMd5
New project: QmW8RzBfgcbBSA7Vo4xGR6Abx2RG8CBPRn2ZooqvG2mjnN
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmVfe9eFWTRbEmpKP7ySrSVf9xuZKB1e8ToVM8ECNDCMd5`)

```
docker container rm -f query_qmvfe9efwtrbemp && docker container rm -f node_qmvfe9efwtrbemp
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmvfe9efwtrbemp RENAME TO schema_qmw8rzbfgcbbsa7;"

```

 3) Run new project from coordinator (`QmW8RzBfgcbBSA7Vo4xGR6Abx2RG8CBPRn2ZooqvG2mjnN`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmvfe9efwtrbemp RENAME TO schema_qmw8rzbfgcbbsa7;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
