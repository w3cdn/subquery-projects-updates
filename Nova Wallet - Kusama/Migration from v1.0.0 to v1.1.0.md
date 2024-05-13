# Migration from v1.0.0 to v1.1.0
```
Old project: QmNr5DAJ7dQ51hB8J2jeQeSvvGwUQ8dFQYojvu9syMqMoQ
New project: QmZMEXCEKgezVUXVXVSHTdiQUhfnYQTH98uz6XCXjA5F6V
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmNr5DAJ7dQ51hB8J2jeQeSvvGwUQ8dFQYojvu9syMqMoQ`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmnr5daj7dq51hb RENAME TO schema_qmzmexcekgezvux;"
```
 3) Run new project from coordinator (`QmZMEXCEKgezVUXVXVSHTdiQUhfnYQTH98uz6XCXjA5F6V`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmnr5daj7dq51hb RENAME TO schema_qmzmexcekgezvux;`
