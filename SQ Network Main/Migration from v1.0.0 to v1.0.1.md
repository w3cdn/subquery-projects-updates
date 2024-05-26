# Migration from v1.0.0 to v1.0.1
```
Old project: QmTMphPvRg143xWWKsdgZZgNc1HgDxH9fK9ZYpzLiQPet1
New project: QmZ5V3iNeivVvYVfr8Ui8XweXNwA98KpEo1rg55XiFvCbz
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmTMphPvRg143xWWKsdgZZgNc1HgDxH9fK9ZYpzLiQPet1`)

```
docker container rm -f query_qmtmphpvrg143xw && docker container rm -f node_qmtmphpvrg143xw
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmtmphpvrg143xw RENAME TO schema_qmz5v3ineivvvyv;"

```

 3) Run new project from coordinator (`QmZ5V3iNeivVvYVfr8Ui8XweXNwA98KpEo1rg55XiFvCbz`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmtmphpvrg143xw RENAME TO schema_qmz5v3ineivvvyv;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
