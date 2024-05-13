# Migration from v1.0.0 to v1.0.1
```
Old project: QmNr5DAJ7dQ51hB8J2jeQeSvvGwUQ8dFQYojvu9syMqMoQ
New project: QmVCeEq87zp1xNfTAKn7Zwy5ixh17rJbWR2LmJ4VJ7onJx
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmNr5DAJ7dQ51hB8J2jeQeSvvGwUQ8dFQYojvu9syMqMoQ`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmnr5daj7dq51hb RENAME TO schema_qmvceeq87zp1xnf;"
```
 3) Run new project from coordinator (`QmVCeEq87zp1xNfTAKn7Zwy5ixh17rJbWR2LmJ4VJ7onJx`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmnr5daj7dq51hb RENAME TO schema_qmvceeq87zp1xnf;`
