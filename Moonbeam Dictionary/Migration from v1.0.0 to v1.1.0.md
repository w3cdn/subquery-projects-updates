# Migration from v1.0.0 to v1.1.0
```
Old project: QmeeqBHdVu7iYnhVE9ZiYEKTWe4jXVUD5pVoGXT6LbCP2t
New project: QmUHAsweQYXYrY5Swbt1eHkUwnE5iLc7w9Fh62JY6guXEK
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmeeqBHdVu7iYnhVE9ZiYEKTWe4jXVUD5pVoGXT6LbCP2t`)

```
docker container rm -f query_qmeeqbhdvu7iynh && docker container rm -f node_qmeeqbhdvu7iynh
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmeeqbhdvu7iynh RENAME TO schema_qmuhasweqyxyry5;"

```

 3) Run new project from coordinator (`QmUHAsweQYXYrY5Swbt1eHkUwnE5iLc7w9Fh62JY6guXEK`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmeeqbhdvu7iynh RENAME TO schema_qmuhasweqyxyry5;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)