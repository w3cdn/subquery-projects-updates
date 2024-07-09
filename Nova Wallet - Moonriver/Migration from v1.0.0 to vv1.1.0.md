# Migration from v1.0.0 to vv1.1.0
```
Old project: QmPzEH1Juo7RQB2X37DvYATQdCQ7oBV8V1yX92DHD71ma5
New project: QmdbhaQ6mFJNHVk5WbNyFsevfJysiXyueMRHqWN7FTXMtN
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmPzEH1Juo7RQB2X37DvYATQdCQ7oBV8V1yX92DHD71ma5`)

```
docker container rm -f query_qmpzeh1juo7rqb2 && docker container rm -f node_qmpzeh1juo7rqb2
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmpzeh1juo7rqb2 RENAME TO schema_qmdbhaq6mfjnhvk;"

```

 3) Run new project from coordinator (`QmdbhaQ6mFJNHVk5WbNyFsevfJysiXyueMRHqWN7FTXMtN`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmpzeh1juo7rqb2 RENAME TO schema_qmdbhaq6mfjnhvk;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
