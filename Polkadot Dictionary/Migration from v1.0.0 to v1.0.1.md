# Migration from v1.0.0 to v1.0.1
```
Old project: QmZGAZQ7e1oZgfuK4V29Fa5gveYK3G2zEwvUzTZKNvSBsm
New project: QmUGBdhQKnzE8q6x6MPqP6LNZGa8gzXf5gkdmhzWjdFGfL
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmZGAZQ7e1oZgfuK4V29Fa5gveYK3G2zEwvUzTZKNvSBsm`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmzgazq7e1ozgfu RENAME TO schema_qmugbdhqknze8q6;"
```
 3) Run new project from coordinator (`QmUGBdhQKnzE8q6x6MPqP6LNZGa8gzXf5gkdmhzWjdFGfL`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmzgazq7e1ozgfu RENAME TO schema_qmugbdhqknze8q6;`
