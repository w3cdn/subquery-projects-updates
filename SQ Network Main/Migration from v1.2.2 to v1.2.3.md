# Migration from v1.2.2 to v1.2.3
```
Old project: QmbmoPYVnJ8sh7mJRBS4dJGQM8nndufE32oNAoQaKxhwVH
New project: QmULvX7eUVbyBzPqFJs1A8udTRMtkUZWjYK5BZD5hMztMt
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmbmoPYVnJ8sh7mJRBS4dJGQM8nndufE32oNAoQaKxhwVH`)

```
docker container rm -f query_qmbmopyvnj8sh7m && docker container rm -f node_qmbmopyvnj8sh7m
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmbmopyvnj8sh7m RENAME TO schema_qmulvx7euvbybzp;"

```

 3) Run new project from coordinator (`QmULvX7eUVbyBzPqFJs1A8udTRMtkUZWjYK5BZD5hMztMt`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmbmopyvnj8sh7m RENAME TO schema_qmulvx7euvbybzp;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
