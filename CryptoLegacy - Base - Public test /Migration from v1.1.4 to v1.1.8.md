# Migration from v1.1.4 to v1.1.8
```
Old project: QmW8RzBfgcbBSA7Vo4xGR6Abx2RG8CBPRn2ZooqvG2mjnN
New project: Qme31RLN8N5z9weeceHTRvvVBr4xReX2wQxpV6Rp2CkppT
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmW8RzBfgcbBSA7Vo4xGR6Abx2RG8CBPRn2ZooqvG2mjnN`)

```
docker container rm -f query_qmw8rzbfgcbbsa7 && docker container rm -f node_qmw8rzbfgcbbsa7
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmw8rzbfgcbbsa7 RENAME TO schema_qme31rln8n5z9we;"

```

 3) Run new project from coordinator (`Qme31RLN8N5z9weeceHTRvvVBr4xReX2wQxpV6Rp2CkppT`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmw8rzbfgcbbsa7 RENAME TO schema_qme31rln8n5z9we;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
