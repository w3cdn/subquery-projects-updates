# Migration from v1.0.0 to v1.1.0
```
Old project: QmXp3MdCjZyUsmXhFXJTisxQiP1P96sm81WGmu2ew7v8WN
New project: QmaYR3CJyhywww1Cf5TMJP15DAcD3YE9ZSNmdLbM7KiQHi
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmXp3MdCjZyUsmXhFXJTisxQiP1P96sm81WGmu2ew7v8WN`)

```
docker container rm -f query_qmxp3mdcjzyusmxdocker container rm -f node_qmxp3mdcjzyusmx
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmxp3mdcjzyusmx RENAME TO schema_qmayr3cjyhywww1;"

```

 3) Run new project from coordinator (`QmaYR3CJyhywww1Cf5TMJP15DAcD3YE9ZSNmdLbM7KiQHi`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmxp3mdcjzyusmx RENAME TO schema_qmayr3cjyhywww1;`
