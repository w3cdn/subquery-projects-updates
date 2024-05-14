# Migration from v1.0.0 to v1.1.0
```
Old project: QmV25WVPgdmAgRCqkbGUU49xdeg9td3CK5LbtBjeQEMxTW
New project: QmPiTswpMTeipwnmJkAcwkcg5Se8XfrucGYVKbwuAxQgJ6
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmV25WVPgdmAgRCqkbGUU49xdeg9td3CK5LbtBjeQEMxTW`)
 
```
docker container rm -f query_qmv25wvpgdmagrcdocker container rm -f node_qmv25wvpgdmagrc```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmv25wvpgdmagrc RENAME TO schema_qmpitswpmteipwn;"
```

 3) Run new project from coordinator (`QmPiTswpMTeipwnmJkAcwkcg5Se8XfrucGYVKbwuAxQgJ6`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmv25wvpgdmagrc RENAME TO schema_qmpitswpmteipwn;`
