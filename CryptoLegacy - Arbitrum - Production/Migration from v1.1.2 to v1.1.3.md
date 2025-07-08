# Migration from v1.1.2 to v1.1.3
```
Old project: QmcY8mBRwkjvXJCuoz9tMxuoELQgWBHxqbST1NfGyeXKjp
New project: QmUm1ixPA9g5zuoSJiAjSNthVurnX8ytELjz2FYBdQdk3D
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmcY8mBRwkjvXJCuoz9tMxuoELQgWBHxqbST1NfGyeXKjp`)

```
docker container rm -f query_qmcy8mbrwkjvxjc && docker container rm -f node_qmcy8mbrwkjvxjc
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmcy8mbrwkjvxjc RENAME TO schema_qmum1ixpa9g5zuo;"

```

 3) Run new project from coordinator (`QmUm1ixPA9g5zuoSJiAjSNthVurnX8ytELjz2FYBdQdk3D`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmcy8mbrwkjvxjc RENAME TO schema_qmum1ixpa9g5zuo;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
