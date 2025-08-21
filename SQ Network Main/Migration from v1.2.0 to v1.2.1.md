# Migration from v1.2.0 to v1.2.1
```
Old project: QmUQy6VqsLgKNGyRrrKQdMnwGdvFD2nfgEKeTJq8G4oqAB
New project: QmVY6DSb4BmEo8zeFH3ZyX3kVg9WKMdWq2vm5YcAdt9FV2
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUQy6VqsLgKNGyRrrKQdMnwGdvFD2nfgEKeTJq8G4oqAB`)

```
docker container rm -f query_qmuqy6vqslgkngy && docker container rm -f node_qmuqy6vqslgkngy
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmuqy6vqslgkngy RENAME TO schema_qmvy6dsb4bmeo8z;"

```

 3) Run new project from coordinator (`QmVY6DSb4BmEo8zeFH3ZyX3kVg9WKMdWq2vm5YcAdt9FV2`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmuqy6vqslgkngy RENAME TO schema_qmvy6dsb4bmeo8z;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
