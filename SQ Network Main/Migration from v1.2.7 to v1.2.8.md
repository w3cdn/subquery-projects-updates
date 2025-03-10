# Migration from v1.2.7 to v1.2.8
```
Old project: QmWaV7Be6KwdhU6v6tUaVCyb1R3rUxYX987fGNJkQ4QisU
New project: QmNfHk9n4KPJJkiJ2WA4hjd3Zpk6d2tR52WeFEtxqgK6Ck
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWaV7Be6KwdhU6v6tUaVCyb1R3rUxYX987fGNJkQ4QisU`)

```
docker container rm -f query_qmwav7be6kwdhu6 && docker container rm -f node_qmwav7be6kwdhu6
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmwav7be6kwdhu6 RENAME TO schema_qmnfhk9n4kpjjki;"

```

 3) Run new project from coordinator (`QmNfHk9n4KPJJkiJ2WA4hjd3Zpk6d2tR52WeFEtxqgK6Ck`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmwav7be6kwdhu6 RENAME TO schema_qmnfhk9n4kpjjki;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
