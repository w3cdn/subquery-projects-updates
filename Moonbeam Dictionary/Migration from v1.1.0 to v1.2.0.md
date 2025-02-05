# Migration from v1.1.0 to v1.2.0
```
Old project: QmUHAsweQYXYrY5Swbt1eHkUwnE5iLc7w9Fh62JY6guXEK
New project: QmTK8vHsfTAoTZyYkiQruhKuwCb2bypj3PnFBcvxJFMJtQ
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUHAsweQYXYrY5Swbt1eHkUwnE5iLc7w9Fh62JY6guXEK`)

```
docker container rm -f query_qmuhasweqyxyry5 && docker container rm -f node_qmuhasweqyxyry5
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmuhasweqyxyry5 RENAME TO schema_qmtk8vhsftaotzy;"

```

 3) Run new project from coordinator (`QmTK8vHsfTAoTZyYkiQruhKuwCb2bypj3PnFBcvxJFMJtQ`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmuhasweqyxyry5 RENAME TO schema_qmtk8vhsftaotzy;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
