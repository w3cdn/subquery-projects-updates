# Migration from v1.0.0 to v1.1.0
```
Old project: QmegTE8BimTw5iTpBqtJSMC2jWApU4g2q5ojGZAL3iU1fr
New project: QmWmm1teaAzm699PBQQ6MuEEmbNJubXHyTpWqCWKurqSNs
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmegTE8BimTw5iTpBqtJSMC2jWApU4g2q5ojGZAL3iU1fr`)

```
docker container rm -f query_qmegte8bimtw5it && docker container rm -f node_qmegte8bimtw5it
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmegte8bimtw5it RENAME TO schema_qmwmm1teaazm699;"

```

 3) Run new project from coordinator (`QmWmm1teaAzm699PBQQ6MuEEmbNJubXHyTpWqCWKurqSNs`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmegte8bimtw5it RENAME TO schema_qmwmm1teaazm699;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
