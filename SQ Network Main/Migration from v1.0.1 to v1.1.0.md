# Migration from v1.0.1 to v1.1.0
```
Old project: QmZ5V3iNeivVvYVfr8Ui8XweXNwA98KpEo1rg55XiFvCbz
New project: QmZdLhKt44hmW56YS63rwr1NbkyGuG224oHjFypeXUiahW
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZ5V3iNeivVvYVfr8Ui8XweXNwA98KpEo1rg55XiFvCbz`)
```
docker container rm -f query_qmz5v3ineivvvyvdocker container rm -f node_qmz5v3ineivvvyv```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmz5v3ineivvvyv RENAME TO schema_qmzdlhkt44hmw56;"
```

 3) Run new project from coordinator (`QmZdLhKt44hmW56YS63rwr1NbkyGuG224oHjFypeXUiahW`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmz5v3ineivvvyv RENAME TO schema_qmzdlhkt44hmw56;`
