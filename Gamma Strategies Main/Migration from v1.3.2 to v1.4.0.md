# Migration from v1.3.2 to v1.4.0
```
Old project: Qmc4x6RFdtHiHcZAc3SfGUS5VwyJMopUswm5GhjW4WucvN
New project: QmVoq3EJUMn63fB5AJ2uiK1XMmxY4XVMmk7kyZpsbkRMji
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmc4x6RFdtHiHcZAc3SfGUS5VwyJMopUswm5GhjW4WucvN`)

```
docker container rm -f query_qmc4x6rfdthihcz && docker container rm -f node_qmc4x6rfdthihcz
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmc4x6rfdthihcz RENAME TO schema_qmvoq3ejumn63fb;"

```

 3) Run new project from coordinator (`QmVoq3EJUMn63fB5AJ2uiK1XMmxY4XVMmk7kyZpsbkRMji`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmc4x6rfdthihcz RENAME TO schema_qmvoq3ejumn63fb;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
