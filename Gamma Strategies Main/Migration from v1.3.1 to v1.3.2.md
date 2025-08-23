# Migration from v1.3.1 to v1.3.2
```
Old project: QmRzvBkdKn9AXyQxAMobZa7EKdP6U3p8RZc7JGwAWs478z
New project: Qmc4x6RFdtHiHcZAc3SfGUS5VwyJMopUswm5GhjW4WucvN
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmRzvBkdKn9AXyQxAMobZa7EKdP6U3p8RZc7JGwAWs478z`)

```
docker container rm -f query_qmrzvbkdkn9axyq && docker container rm -f node_qmrzvbkdkn9axyq
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmrzvbkdkn9axyq RENAME TO schema_qmc4x6rfdthihcz;"

```

 3) Run new project from coordinator (`Qmc4x6RFdtHiHcZAc3SfGUS5VwyJMopUswm5GhjW4WucvN`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmrzvbkdkn9axyq RENAME TO schema_qmc4x6rfdthihcz;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
