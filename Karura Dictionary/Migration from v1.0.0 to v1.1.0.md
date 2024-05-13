# Migration from v1.0.0 to v1.1.0
```
Old project: QmZUynW4WfM5hmQdTxJb9o6xLEU7jTViWXkb4fwiM5VxX2
New project: Qmdw5d7XsR52bfXzZmxCHoTfJJZeT4c4K1ppqMgwVQVos8
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZUynW4WfM5hmQdTxJb9o6xLEU7jTViWXkb4fwiM5VxX2`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmzuynw4wfm5hmq RENAME TO schema_qmdw5d7xsr52bfx;"
```
 3) Run new project from coordinator (`Qmdw5d7XsR52bfXzZmxCHoTfJJZeT4c4K1ppqMgwVQVos8`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmzuynw4wfm5hmq RENAME TO schema_qmdw5d7xsr52bfx;`
