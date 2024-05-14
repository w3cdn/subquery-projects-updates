# Migration from v1.0.0 to v1.1.0
```
Old project: Qmc9svij5SxCEGApMZzV9MwWgy8TuMTtGgsrWxR1yaUqZ9
New project: QmeBTNuhahUo2EhTRxV3qVAVf5bC8zVQRrrHd3SUDXgtbF
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmc9svij5SxCEGApMZzV9MwWgy8TuMTtGgsrWxR1yaUqZ9`)
 
```
docker container rm -f query_qmc9svij5sxcegadocker container rm -f node_qmc9svij5sxcega```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmc9svij5sxcega RENAME TO schema_qmebtnuhahuo2eh;"
```

 3) Run new project from coordinator (`QmeBTNuhahUo2EhTRxV3qVAVf5bC8zVQRrrHd3SUDXgtbF`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmc9svij5sxcega RENAME TO schema_qmebtnuhahuo2eh;`
