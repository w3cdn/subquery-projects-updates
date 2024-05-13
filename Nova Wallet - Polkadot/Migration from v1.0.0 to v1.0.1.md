# Migration from v1.0.0 to v1.0.1
```
Old project: QmNr5DAJ7dQ51hB8J2jeQeSvvGwUQ8dFQYojvu9syMqMoQ
New project: QmeWSK7F1DKJRvD9SnRZtq9qcd1CprsYy45BPRgbc7J9cL
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmNr5DAJ7dQ51hB8J2jeQeSvvGwUQ8dFQYojvu9syMqMoQ`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmnr5daj7dq51hb RENAME TO schema_qmewsk7f1dkjrvd;"
```
 3) Run new project from coordinator (`QmeWSK7F1DKJRvD9SnRZtq9qcd1CprsYy45BPRgbc7J9cL`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmnr5daj7dq51hb RENAME TO schema_qmewsk7f1dkjrvd;`
