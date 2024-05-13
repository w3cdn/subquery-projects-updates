# Migration from v1.0.0 to v1.0.1
```
Old project: QmQu2Lsfd2xNvjAyNs587272h5hWRKxQkC4H66tSEHe9jR
New project: QmSsbTrWMd7iyT7Vk4c2w6j8BUt2mpMtJpZ3DDnHocpyWe
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmQu2Lsfd2xNvjAyNs587272h5hWRKxQkC4H66tSEHe9jR`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmqu2lsfd2xnvja RENAME TO schema_qmssbtrwmd7iyt7;"
```
 3) Run new project from coordinator (`QmSsbTrWMd7iyT7Vk4c2w6j8BUt2mpMtJpZ3DDnHocpyWe`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmqu2lsfd2xnvja RENAME TO schema_qmssbtrwmd7iyt7;`
