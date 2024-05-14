# Migration from v1.0.0 to v1.1.0
```
Old project: QmQtmsHoJEYUcxKE4tBqr9Z8kudcgkczQPfhkAxVExQX5y
New project: QmZpj5wYpUbGqJDg6KWgbkK5bmeuCqYX6kwk317jdJ9DZ4
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmQtmsHoJEYUcxKE4tBqr9Z8kudcgkczQPfhkAxVExQX5y`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmqtmshojeyucxk RENAME TO schema_qmzpj5wypubgqjd;"
```
 3) Run new project from coordinator (`QmZpj5wYpUbGqJDg6KWgbkK5bmeuCqYX6kwk317jdJ9DZ4`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmqtmshojeyucxk RENAME TO schema_qmzpj5wypubgqjd;`
