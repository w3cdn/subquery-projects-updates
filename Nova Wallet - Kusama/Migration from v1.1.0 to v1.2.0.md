# Migration from v1.1.0 to v1.2.0
```
Old project: QmZMEXCEKgezVUXVXVSHTdiQUhfnYQTH98uz6XCXjA5F6V
New project: QmZ7C68DBApnHDagcCcUsCWkGViB6nsqMy1tacji2nfMEo
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZMEXCEKgezVUXVXVSHTdiQUhfnYQTH98uz6XCXjA5F6V`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmzmexcekgezvux RENAME TO schema_qmz7c68dbapnhda;"
```
 3) Run new project from coordinator (`QmZ7C68DBApnHDagcCcUsCWkGViB6nsqMy1tacji2nfMEo`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmzmexcekgezvux RENAME TO schema_qmz7c68dbapnhda;`
