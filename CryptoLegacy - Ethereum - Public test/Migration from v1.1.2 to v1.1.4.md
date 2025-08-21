# Migration from v1.1.2 to v1.1.4
```
Old project: QmYPxDRgnsR4uprwrRUHvd6oMHr1bdjbDMesSKh4M2kSiH
New project: QmUK1PBK3QsU8Gq897QeaJ9JhHmkk8RRxkotdvZa5MRYwD
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmYPxDRgnsR4uprwrRUHvd6oMHr1bdjbDMesSKh4M2kSiH`)

```
docker container rm -f query_qmypxdrgnsr4upr && docker container rm -f node_qmypxdrgnsr4upr
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmypxdrgnsr4upr RENAME TO schema_qmuk1pbk3qsu8gq;"

```

 3) Run new project from coordinator (`QmUK1PBK3QsU8Gq897QeaJ9JhHmkk8RRxkotdvZa5MRYwD`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmypxdrgnsr4upr RENAME TO schema_qmuk1pbk3qsu8gq;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
