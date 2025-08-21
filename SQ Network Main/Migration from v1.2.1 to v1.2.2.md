# Migration from v1.2.1 to v1.2.2
```
Old project: QmVY6DSb4BmEo8zeFH3ZyX3kVg9WKMdWq2vm5YcAdt9FV2
New project: QmbmoPYVnJ8sh7mJRBS4dJGQM8nndufE32oNAoQaKxhwVH
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmVY6DSb4BmEo8zeFH3ZyX3kVg9WKMdWq2vm5YcAdt9FV2`)

```
docker container rm -f query_qmvy6dsb4bmeo8z && docker container rm -f node_qmvy6dsb4bmeo8z
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmvy6dsb4bmeo8z RENAME TO schema_qmbmopyvnj8sh7m;"

```

 3) Run new project from coordinator (`QmbmoPYVnJ8sh7mJRBS4dJGQM8nndufE32oNAoQaKxhwVH`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmvy6dsb4bmeo8z RENAME TO schema_qmbmopyvnj8sh7m;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
