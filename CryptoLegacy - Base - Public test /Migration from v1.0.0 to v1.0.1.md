# Migration from v1.0.0 to v1.0.1
```
Old project: QmNy7HS61sE2Q5vay6uMYM2sugNyaWPFcQjWSjewBSwg4P
New project: QmRWsgsKkjayJ4eK4yhXHTSXWYVE41AUatAWy9udch1hcQ
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmNy7HS61sE2Q5vay6uMYM2sugNyaWPFcQjWSjewBSwg4P`)

```
docker container rm -f query_qmny7hs61se2q5v && docker container rm -f node_qmny7hs61se2q5v
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmny7hs61se2q5v RENAME TO schema_qmrwsgskkjayj4e;"

```

 3) Run new project from coordinator (`QmRWsgsKkjayJ4eK4yhXHTSXWYVE41AUatAWy9udch1hcQ`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmny7hs61se2q5v RENAME TO schema_qmrwsgskkjayj4e;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
