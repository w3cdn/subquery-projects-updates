# Migration from v1.0.0 to v1.1.0
```
Old project: QmUmnKPhcE6JwGMYvY3Yitb5j8qxbQBMxgpkHpVQuXqxDH
New project: QmapQ6cNKPtZE1jkeUp5V6xy7sPSiJiZpoqZcRRtyc4Stq
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUmnKPhcE6JwGMYvY3Yitb5j8qxbQBMxgpkHpVQuXqxDH`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmumnkphce6jwgm RENAME TO schema_qmapq6cnkptze1j;"
```
 3) Run new project from coordinator (`QmapQ6cNKPtZE1jkeUp5V6xy7sPSiJiZpoqZcRRtyc4Stq`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmumnkphce6jwgm RENAME TO schema_qmapq6cnkptze1j;`
