# Migration from v1.2.0 to v1.3.0
```
Old project: Qmea9t8EGmHenMwAvhiYyzANYobGLNb37E6bs5QzZFxtiX
New project: QmfVyLpFjkvT7DKU8hdqBpxKR677ak6bo7jeU68XsCPHLZ
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmea9t8EGmHenMwAvhiYyzANYobGLNb37E6bs5QzZFxtiX`)

```
docker container rm -f query_qmea9t8egmhenmw && docker container rm -f node_qmea9t8egmhenmw
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmea9t8egmhenmw RENAME TO schema_qmfvylpfjkvt7dk;"

```

 3) Run new project from coordinator (`QmfVyLpFjkvT7DKU8hdqBpxKR677ak6bo7jeU68XsCPHLZ`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmea9t8egmhenmw RENAME TO schema_qmfvylpfjkvt7dk;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
