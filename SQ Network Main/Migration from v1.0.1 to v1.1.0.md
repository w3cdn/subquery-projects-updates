# Migration from v1.0.1 to v1.1.0
```
Old project: Qmb1TTm3xkTBHikQE3QMfVDjszg2dHDir7mZMQS5c4MkDL
New project: QmedqtyGqvwzv6Gw6vL7bhy2CnmWzQ9eXCd2YWWnY75yEu
```


## Upgrade instructions
 1) Stop old project from coordinator (`Qmb1TTm3xkTBHikQE3QMfVDjszg2dHDir7mZMQS5c4MkDL`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmb1ttm3xktbhik RENAME TO schema_qmedqtygqvwzv6g;"
```
 3) Run new project from coordinator (`QmedqtyGqvwzv6Gw6vL7bhy2CnmWzQ9eXCd2YWWnY75yEu`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmb1ttm3xktbhik RENAME TO schema_qmedqtygqvwzv6g;`
