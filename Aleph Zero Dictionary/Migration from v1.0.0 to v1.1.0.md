# Migration from v1.0.0 to v1.1.0
```
Old project: QmXp3MdCjZyUsmXhFXJTisxQiP1P96sm81WGmu2ew7v8WN
New project: QmaYR3CJyhywww1Cf5TMJP15DAcD3YE9ZSNmdLbM7KiQHi
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmXp3MdCjZyUsmXhFXJTisxQiP1P96sm81WGmu2ew7v8WN`)

```
docker container rm -f query_qmxp3mdcjzyusmx && docker container rm -f node_qmxp3mdcjzyusmx
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmxp3mdcjzyusmx RENAME TO schema_qmayr3cjyhywww1;"

```

 3) Run new project from coordinator (`QmaYR3CJyhywww1Cf5TMJP15DAcD3YE9ZSNmdLbM7KiQHi`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmxp3mdcjzyusmx RENAME TO schema_qmayr3cjyhywww1;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
