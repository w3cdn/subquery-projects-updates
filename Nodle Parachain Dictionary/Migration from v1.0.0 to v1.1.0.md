# Migration from v1.0.0 to v1.1.0
```
Old project: QmQtmsHoJEYUcxKE4tBqr9Z8kudcgkczQPfhkAxVExQX5y
New project: QmZpj5wYpUbGqJDg6KWgbkK5bmeuCqYX6kwk317jdJ9DZ4
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmQtmsHoJEYUcxKE4tBqr9Z8kudcgkczQPfhkAxVExQX5y`)

```
docker container rm -f query_qmqtmshojeyucxk && docker container rm -f node_qmqtmshojeyucxk
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmqtmshojeyucxk RENAME TO schema_qmzpj5wypubgqjd;"

```

 3) Run new project from coordinator (`QmZpj5wYpUbGqJDg6KWgbkK5bmeuCqYX6kwk317jdJ9DZ4`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmqtmshojeyucxk RENAME TO schema_qmzpj5wypubgqjd;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
