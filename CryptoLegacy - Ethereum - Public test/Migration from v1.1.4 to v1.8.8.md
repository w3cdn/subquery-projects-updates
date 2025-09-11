# Migration from v1.1.4 to v1.8.8
```
Old project: QmUK1PBK3QsU8Gq897QeaJ9JhHmkk8RRxkotdvZa5MRYwD
New project: QmYvqcqP73CfwZUPKmrrLgs5iRrB5xn9K3RwSxjyUnChGN
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUK1PBK3QsU8Gq897QeaJ9JhHmkk8RRxkotdvZa5MRYwD`)

```
docker container rm -f query_qmuk1pbk3qsu8gq && docker container rm -f node_qmuk1pbk3qsu8gq
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmuk1pbk3qsu8gq RENAME TO schema_qmyvqcqp73cfwzu;"

```

 3) Run new project from coordinator (`QmYvqcqP73CfwZUPKmrrLgs5iRrB5xn9K3RwSxjyUnChGN`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmuk1pbk3qsu8gq RENAME TO schema_qmyvqcqp73cfwzu;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
