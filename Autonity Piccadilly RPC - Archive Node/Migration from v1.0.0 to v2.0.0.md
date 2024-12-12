# Migration from v1.0.0 to v2.0.0
```
Old project: QmW5RcoyWKRJdrgV1aGair8UtGZhpfK4VrYJvs4sRzGVL2
New project: QmSXV8pkxKufQNGdaJ2N15t4cCta4iYWL7QXdLvtjEaS48
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmW5RcoyWKRJdrgV1aGair8UtGZhpfK4VrYJvs4sRzGVL2`)

```
docker container rm -f query_qmw5rcoywkrjdrg && docker container rm -f node_qmw5rcoywkrjdrg
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmw5rcoywkrjdrg RENAME TO schema_qmsxv8pkxkufqng;"

```

 3) Run new project from coordinator (`QmSXV8pkxKufQNGdaJ2N15t4cCta4iYWL7QXdLvtjEaS48`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmw5rcoywkrjdrg RENAME TO schema_qmsxv8pkxkufqng;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
