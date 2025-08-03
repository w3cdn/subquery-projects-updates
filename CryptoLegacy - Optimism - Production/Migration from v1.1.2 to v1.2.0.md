# Migration from v1.1.2 to v1.2.0
```
Old project: QmfDniPfxf1LvRu9Zhjx9w81Z7xTupCkgEBG4ooFAac6LN
New project: QmWVb6tpvCkqc38dQ6z8TP8ekZJRd5qfunmLV8UbaswU83
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmfDniPfxf1LvRu9Zhjx9w81Z7xTupCkgEBG4ooFAac6LN`)

```
docker container rm -f query_qmfdnipfxf1lvru && docker container rm -f node_qmfdnipfxf1lvru
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmfdnipfxf1lvru RENAME TO schema_qmwvb6tpvckqc38;"

```

 3) Run new project from coordinator (`QmWVb6tpvCkqc38dQ6z8TP8ekZJRd5qfunmLV8UbaswU83`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmfdnipfxf1lvru RENAME TO schema_qmwvb6tpvckqc38;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
