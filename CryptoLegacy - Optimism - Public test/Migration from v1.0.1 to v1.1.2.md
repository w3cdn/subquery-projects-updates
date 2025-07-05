# Migration from v1.0.1 to v1.1.2
```
Old project: QmSjQfS5nG3oGPFNu4WLspwgp6LT9nPPQvf1hh9wSn5m77
New project: Qmbpcmu5FBjXDvUBJ8BNEddqz31dLWsqp42QQ66Vt1SEGD
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmSjQfS5nG3oGPFNu4WLspwgp6LT9nPPQvf1hh9wSn5m77`)

```
docker container rm -f query_qmsjqfs5ng3ogpf && docker container rm -f node_qmsjqfs5ng3ogpf
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmsjqfs5ng3ogpf RENAME TO schema_qmbpcmu5fbjxdvu;"

```

 3) Run new project from coordinator (`Qmbpcmu5FBjXDvUBJ8BNEddqz31dLWsqp42QQ66Vt1SEGD`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmsjqfs5ng3ogpf RENAME TO schema_qmbpcmu5fbjxdvu;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subqueryprojectsupdates](https://t.me/subqueryprojectsupdates) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
