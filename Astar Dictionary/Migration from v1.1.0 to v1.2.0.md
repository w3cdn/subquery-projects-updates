# Migration from v1.1.0 to v1.2.0
```
Old project: QmapQ6cNKPtZE1jkeUp5V6xy7sPSiJiZpoqZcRRtyc4Stq
New project: Qmf11zTwkTAkNVdd6paDmfJ9CKzcrF2jp6febb52Xoo2wX
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmapQ6cNKPtZE1jkeUp5V6xy7sPSiJiZpoqZcRRtyc4Stq`)

```
docker container rm -f query_qmapq6cnkptze1j && docker container rm -f node_qmapq6cnkptze1j
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmapq6cnkptze1j RENAME TO schema_qmf11ztwktaknvd;"

```

 3) Run new project from coordinator (`Qmf11zTwkTAkNVdd6paDmfJ9CKzcrF2jp6febb52Xoo2wX`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmapq6cnkptze1j RENAME TO schema_qmf11ztwktaknvd;`


___
### Setup your own indexer:

[https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/w3cdn/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://t.me/subquery_projects_tracker](https://t.me/subquery_projects_tracker) [https://eagleeye.subquery.dev/updates](https://eagleeye.subquery.dev/updates)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot) [https://eagleeye.subquery.dev/](https://eagleeye.subquery.dev/)


### Subquery Indexers Snapshots:

[https://snapshots.subquery.dev/](https://snapshots.subquery.dev/)
