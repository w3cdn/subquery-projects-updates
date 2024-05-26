# Migration from v1.0.0 to v1.1.0
```
Old project: QmWumrabg4k6t4EUMhQg19xWwcxGq1hWbcmfmRYiy2Bod5
New project: QmPQQA28fxR1hePk25MHNS1vEYRs4Gbz3PXry8G4dfC76N
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWumrabg4k6t4EUMhQg19xWwcxGq1hWbcmfmRYiy2Bod5`)

```
docker container rm -f query_qmwumrabg4k6t4e && docker container rm -f node_qmwumrabg4k6t4e
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmwumrabg4k6t4e RENAME TO schema_qmpqqa28fxr1hep;"

```

 3) Run new project from coordinator (`QmPQQA28fxR1hePk25MHNS1vEYRs4Gbz3PXry8G4dfC76N`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmwumrabg4k6t4e RENAME TO schema_qmpqqa28fxr1hep;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
