# Migration from v1.0.0 to v1.1.0
```
Old project: QmYCAns2cunZKJFU85KNK8CvL2ATAmCFVZRdBf963GqWYs
New project: QmP2KRbGx4vLaL8HqugVXrNPMyziFL6aM9NAd4NbFqsPA9
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmYCAns2cunZKJFU85KNK8CvL2ATAmCFVZRdBf963GqWYs`)

```
docker container rm -f query_qmycans2cunzkjfdocker container rm -f node_qmycans2cunzkjf
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmycans2cunzkjf RENAME TO schema_qmp2krbgx4vlal8;"

```

 3) Run new project from coordinator (`QmP2KRbGx4vLaL8HqugVXrNPMyziFL6aM9NAd4NbFqsPA9`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmycans2cunzkjf RENAME TO schema_qmp2krbgx4vlal8;`
