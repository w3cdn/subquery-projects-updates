# Migration from v1.0.0 to v1.1.0
```
Old project: QmXCr6uZFdY1YcGTa4u6ZieQPXK4VHE1Pjy7CBr7ubFwKR
New project: QmWhwLQA4P6iZv6bmQxUqG5zumNK8KDBwcq8wxN4G213dq
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmXCr6uZFdY1YcGTa4u6ZieQPXK4VHE1Pjy7CBr7ubFwKR`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmxcr6uzfdy1ycg RENAME TO schema_qmwhwlqa4p6izv6;"
```
 3) Run new project from coordinator (`QmWhwLQA4P6iZv6bmQxUqG5zumNK8KDBwcq8wxN4G213dq`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmxcr6uzfdy1ycg RENAME TO schema_qmwhwlqa4p6izv6;`
