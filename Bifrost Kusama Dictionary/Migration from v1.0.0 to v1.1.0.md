# Migration from v1.0.0 to v1.1.0
```
Old project: QmZUynW4WfM5hmQdTxJb9o6xLEU7jTViWXkb4fwiM5VxX2
New project: QmeqwHYeFUemUTJPvv9tkeuRAfMNfPfiZdzQECPL7uU2Lj
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZUynW4WfM5hmQdTxJb9o6xLEU7jTViWXkb4fwiM5VxX2`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmzuynw4wfm5hmq RENAME TO schema_qmeqwhyefuemutj;"
```
 3) Run new project from coordinator (`QmeqwHYeFUemUTJPvv9tkeuRAfMNfPfiZdzQECPL7uU2Lj`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmzuynw4wfm5hmq RENAME TO schema_qmeqwhyefuemutj;`
