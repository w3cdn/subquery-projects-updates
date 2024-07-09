# Migration from v1.0.0 to v1.1.0
```
Old project: QmPeUqCW1Sf3gz9JKbLy48pi1a5mcmeqC2WR8opTHNjn3V
New project: QmVKG3gJejcPwKXHP1Yhk1tVTzKh4EZshpJSQyFtCeZkhc
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmPeUqCW1Sf3gz9JKbLy48pi1a5mcmeqC2WR8opTHNjn3V`)

```
docker container rm -f query_qmpeuqcw1sf3gz9 && docker container rm -f node_qmpeuqcw1sf3gz9
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmpeuqcw1sf3gz9 RENAME TO schema_qmvkg3gjejcpwkx;"

```

 3) Run new project from coordinator (`QmVKG3gJejcPwKXHP1Yhk1tVTzKh4EZshpJSQyFtCeZkhc`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmpeuqcw1sf3gz9 RENAME TO schema_qmvkg3gjejcpwkx;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
