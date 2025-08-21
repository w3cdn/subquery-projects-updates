# Migration from v1.0.0 to v1.1.0
```
Old project: QmYNRtrcD2QKftkff2UpjV3fr3ubPZuYahTNDAct4Ad2NW
New project: QmaGmVYRd4oMBJdTMwWLhduzE3Je5HkxY9babkELnbo5Tv
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmYNRtrcD2QKftkff2UpjV3fr3ubPZuYahTNDAct4Ad2NW`)

```
docker container rm -f query_qmynrtrcd2qkftk && docker container rm -f node_qmynrtrcd2qkftk
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmynrtrcd2qkftk RENAME TO schema_qmagmvyrd4ombjd;"

```

 3) Run new project from coordinator (`QmaGmVYRd4oMBJdTMwWLhduzE3Je5HkxY9babkELnbo5Tv`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmynrtrcd2qkftk RENAME TO schema_qmagmvyrd4ombjd;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
