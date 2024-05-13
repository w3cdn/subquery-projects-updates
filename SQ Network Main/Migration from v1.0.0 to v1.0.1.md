# Migration from v1.0.0 to v1.0.1
```
Old project: QmSPKqh2wbQ2xpBNDAkkeWF5BTzfPvvjEDwxzoY1pyTMNF
New project: Qmb1TTm3xkTBHikQE3QMfVDjszg2dHDir7mZMQS5c4MkDL
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmSPKqh2wbQ2xpBNDAkkeWF5BTzfPvvjEDwxzoY1pyTMNF`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmspkqh2wbq2xpb RENAME TO schema_qmb1ttm3xktbhik;"
```
 3) Run new project from coordinator (`Qmb1TTm3xkTBHikQE3QMfVDjszg2dHDir7mZMQS5c4MkDL`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmspkqh2wbq2xpb RENAME TO schema_qmb1ttm3xktbhik;`
