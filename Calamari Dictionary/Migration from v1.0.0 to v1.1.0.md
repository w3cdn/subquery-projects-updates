# Migration from v1.0.0 to v1.1.0
```
Old project: QmUpvkmvTRkMDCGDXnAVjCBZLzZEv9UCVKHH2s3gj3hYQK
New project: QmdrqzazvSmrr6rgfxJEssJH9jqhYCZARm92UxNXMv5f86
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUpvkmvTRkMDCGDXnAVjCBZLzZEv9UCVKHH2s3gj3hYQK`)
 
```
docker container rm -f query_qmupvkmvtrkmdcgdocker container rm -f node_qmupvkmvtrkmdcg```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmupvkmvtrkmdcg RENAME TO schema_qmdrqzazvsmrr6r;"
```

 3) Run new project from coordinator (`QmdrqzazvSmrr6rgfxJEssJH9jqhYCZARm92UxNXMv5f86`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmupvkmvtrkmdcg RENAME TO schema_qmdrqzazvsmrr6r;`
