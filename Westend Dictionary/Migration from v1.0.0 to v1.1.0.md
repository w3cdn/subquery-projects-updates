# Migration from v1.0.0 to v1.1.0
```
Old project: Qma6BeSQGHrhP5aydmkQcJCR25TEwuNMogS5boovBBwoeW
New project: QmP1BMJoyJ5iFq6XLSfTJ3D23iWuTG1tnsEffJpNieQnwN
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qma6BeSQGHrhP5aydmkQcJCR25TEwuNMogS5boovBBwoeW`)
```
docker container rm -f query_qma6besqghrhp5adocker container rm -f node_qma6besqghrhp5a```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qma6besqghrhp5a RENAME TO schema_qmp1bmjoyj5ifq6;"
```

 3) Run new project from coordinator (`QmP1BMJoyJ5iFq6XLSfTJ3D23iWuTG1tnsEffJpNieQnwN`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qma6besqghrhp5a RENAME TO schema_qmp1bmjoyj5ifq6;`
