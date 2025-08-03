# Migration from v1.1.2 to v1.2.0
```
Old project: QmaaXm7m5yg8fX3bGMLGeHQy81bDMHHPw7zV9XXLd7ddqf
New project: QmXPTLREnfNwizBr9di7SBYXkKfiesBYfZQvvmNb6sEvzD
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmaaXm7m5yg8fX3bGMLGeHQy81bDMHHPw7zV9XXLd7ddqf`)

```
docker container rm -f query_qmaaxm7m5yg8fx3 && docker container rm -f node_qmaaxm7m5yg8fx3
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmaaxm7m5yg8fx3 RENAME TO schema_qmxptlrenfnwizb;"

```

 3) Run new project from coordinator (`QmXPTLREnfNwizBr9di7SBYXkKfiesBYfZQvvmNb6sEvzD`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmaaxm7m5yg8fx3 RENAME TO schema_qmxptlrenfnwizb;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
