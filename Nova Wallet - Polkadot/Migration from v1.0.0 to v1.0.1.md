# Migration from v1.0.0 to v1.0.1
```
Old project: QmaTy1aG5uZfeyUXRu8bDci1P6AzbTYBEzM57yEYk3MPEt
New project: QmUSvntAvxr1kUGESMbugxxUJaGRY13JcgG1wDphs3nMeV
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmaTy1aG5uZfeyUXRu8bDci1P6AzbTYBEzM57yEYk3MPEt`)
```
docker container rm -f query_qmaty1ag5uzfeyudocker container rm -f node_qmaty1ag5uzfeyu```
 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmaty1ag5uzfeyu RENAME TO schema_qmusvntavxr1kug;"
```
 3) Run new project from coordinator (`QmUSvntAvxr1kUGESMbugxxUJaGRY13JcgG1wDphs3nMeV`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmaty1ag5uzfeyu RENAME TO schema_qmusvntavxr1kug;`
