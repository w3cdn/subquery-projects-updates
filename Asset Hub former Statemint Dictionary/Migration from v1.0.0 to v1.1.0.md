# Migration from v1.0.0 to v1.1.0
```
Old project: QmckGGY1AhrB75MwPPzR9orgWjwDVF4kXfwkZehZSZxmdE
New project: Qme1iQvwLoeh1ZLZVL4zDGZBK1hnMG3xZz1oaLBRvZxT7X
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmckGGY1AhrB75MwPPzR9orgWjwDVF4kXfwkZehZSZxmdE`)
```
docker container rm -f query_qmckggy1ahrb75mdocker container rm -f node_qmckggy1ahrb75m```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmckggy1ahrb75m RENAME TO schema_qme1iqvwloeh1zl;"
```

 3) Run new project from coordinator (`Qme1iQvwLoeh1ZLZVL4zDGZBK1hnMG3xZz1oaLBRvZxT7X`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmckggy1ahrb75m RENAME TO schema_qme1iqvwloeh1zl;`
