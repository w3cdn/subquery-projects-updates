# Migration from v1.0.0 to v1.1.0
```
Old project: QmZUynW4WfM5hmQdTxJb9o6xLEU7jTViWXkb4fwiM5VxX2
New project: QmZUB7WDyExd88dSca6TzfJgsjsr3iE17Ah9L4Y2DUyLCm
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZUynW4WfM5hmQdTxJb9o6xLEU7jTViWXkb4fwiM5VxX2`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmzuynw4wfm5hmq RENAME TO schema_qmzub7wdyexd88d;"
```
 3) Run new project from coordinator (`QmZUB7WDyExd88dSca6TzfJgsjsr3iE17Ah9L4Y2DUyLCm`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmzuynw4wfm5hmq RENAME TO schema_qmzub7wdyexd88d;`
