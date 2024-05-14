# Migration from v1.0.0 to v1.1.0
```
Old project: undefined
New project: undefined
```


## Upgrade instructions
 1) Stop old project from coordinator (`undefined`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_undefined RENAME TO schema_undefined;"
```
 3) Run new project from coordinator (`undefined`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_undefined RENAME TO schema_undefined;`
