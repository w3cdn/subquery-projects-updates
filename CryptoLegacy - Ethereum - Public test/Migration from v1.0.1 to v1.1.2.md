# Migration from v1.0.1 to v1.1.2
```
Old project: QmRpGB36vEETn8otHh2WTr6VcHU2SVpvGUye7dr1KLFxxN
New project: QmYPxDRgnsR4uprwrRUHvd6oMHr1bdjbDMesSKh4M2kSiH
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmRpGB36vEETn8otHh2WTr6VcHU2SVpvGUye7dr1KLFxxN`)

```
docker container rm -f query_qmrpgb36veetn8o && docker container rm -f node_qmrpgb36veetn8o
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmrpgb36veetn8o RENAME TO schema_qmypxdrgnsr4upr;"

```

 3) Run new project from coordinator (`QmYPxDRgnsR4uprwrRUHvd6oMHr1bdjbDMesSKh4M2kSiH`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmrpgb36veetn8o RENAME TO schema_qmypxdrgnsr4upr;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
