# Migration from v1.0.1 to v1.1.2
```
Old project: QmRWsgsKkjayJ4eK4yhXHTSXWYVE41AUatAWy9udch1hcQ
New project: QmVfe9eFWTRbEmpKP7ySrSVf9xuZKB1e8ToVM8ECNDCMd5
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmRWsgsKkjayJ4eK4yhXHTSXWYVE41AUatAWy9udch1hcQ`)

```
docker container rm -f query_qmrwsgskkjayj4e && docker container rm -f node_qmrwsgskkjayj4e
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmrwsgskkjayj4e RENAME TO schema_qmvfe9efwtrbemp;"

```

 3) Run new project from coordinator (`QmVfe9eFWTRbEmpKP7ySrSVf9xuZKB1e8ToVM8ECNDCMd5`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmrwsgskkjayj4e RENAME TO schema_qmvfe9efwtrbemp;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
