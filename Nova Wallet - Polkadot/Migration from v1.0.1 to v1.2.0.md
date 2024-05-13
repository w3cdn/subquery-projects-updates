# Migration from v1.0.1 to v1.2.0
```
Old project: QmeWSK7F1DKJRvD9SnRZtq9qcd1CprsYy45BPRgbc7J9cL
New project: QmW8UmCcasjPUqaMB3iwbLotDnA4XKMCQ4QFWaSaCKF8fJ
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmeWSK7F1DKJRvD9SnRZtq9qcd1CprsYy45BPRgbc7J9cL`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmewsk7f1dkjrvd RENAME TO schema_qmw8umccasjpuqa;"
```
 3) Run new project from coordinator (`QmW8UmCcasjPUqaMB3iwbLotDnA4XKMCQ4QFWaSaCKF8fJ`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmewsk7f1dkjrvd RENAME TO schema_qmw8umccasjpuqa;`
