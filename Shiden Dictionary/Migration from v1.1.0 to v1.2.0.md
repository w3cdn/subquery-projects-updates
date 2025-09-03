# Migration from v1.1.0 to v1.2.0
```
Old project: QmPiTswpMTeipwnmJkAcwkcg5Se8XfrucGYVKbwuAxQgJ6
New project: QmdrHEvuzynZCXYWQSxxbH6VS1qk9HHVDLKJUAzKWSCYRr
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmPiTswpMTeipwnmJkAcwkcg5Se8XfrucGYVKbwuAxQgJ6`)

```
docker container rm -f query_qmpitswpmteipwn && docker container rm -f node_qmpitswpmteipwn
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmpitswpmteipwn RENAME TO schema_qmdrhevuzynzcxy;"

```

 3) Run new project from coordinator (`QmdrHEvuzynZCXYWQSxxbH6VS1qk9HHVDLKJUAzKWSCYRr`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmpitswpmteipwn RENAME TO schema_qmdrhevuzynzcxy;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
