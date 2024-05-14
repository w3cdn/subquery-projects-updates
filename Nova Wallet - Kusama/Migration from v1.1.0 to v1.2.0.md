# Migration from v1.1.0 to v1.2.0
```
Old project: QmWm7SG64PwYsX5vhmuLbrZ4issMMBVPNFoJSusudDVPzf
New project: QmSCNvH1dPT8AwSMbxbePDe5QNMVre81wHfXgA9MwLrFWF
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWm7SG64PwYsX5vhmuLbrZ4issMMBVPNFoJSusudDVPzf`)

```
docker container rm -f query_qmwm7sg64pwysx5 && docker container rm -f node_qmwm7sg64pwysx5
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmwm7sg64pwysx5 RENAME TO schema_qmscnvh1dpt8aws;"

```

 3) Run new project from coordinator (`QmSCNvH1dPT8AwSMbxbePDe5QNMVre81wHfXgA9MwLrFWF`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmwm7sg64pwysx5 RENAME TO schema_qmscnvh1dpt8aws;`
