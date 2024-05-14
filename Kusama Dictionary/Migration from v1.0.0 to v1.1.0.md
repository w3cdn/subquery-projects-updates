# Migration from v1.0.0 to v1.1.0
```
Old project: QmXwfCF8858YY924VHgNLsxRQfBLosVbB31mygRLhgJbWn
New project: Qmbe5g5vbEJYYAfpjcwNDzuhjeyaEQPQbxKyKx6PveYnR8
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmXwfCF8858YY924VHgNLsxRQfBLosVbB31mygRLhgJbWn`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmxwfcf8858yy92 RENAME TO schema_qmbe5g5vbejyyaf;"
```
 3) Run new project from coordinator (`Qmbe5g5vbEJYYAfpjcwNDzuhjeyaEQPQbxKyKx6PveYnR8`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmxwfcf8858yy92 RENAME TO schema_qmbe5g5vbejyyaf;`
