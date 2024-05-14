# Migration from v1.0.0 to v1.1.0
```
Old project: QmWS4bvLU9Y1YBkrcDBq3Z7enZf8LykeyjSvgVKjB7FSVz
New project: QmWm7SG64PwYsX5vhmuLbrZ4issMMBVPNFoJSusudDVPzf
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmWS4bvLU9Y1YBkrcDBq3Z7enZf8LykeyjSvgVKjB7FSVz`)
 2) Execute query.

```
docker exec postgres psql -U postgres -c "ALTER SCHEMA schema_qmws4bvlu9y1ybk RENAME TO schema_qmwm7sg64pwysx5;"
```
 3) Run new project from coordinator (`QmWm7SG64PwYsX5vhmuLbrZ4issMMBVPNFoJSusudDVPzf`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmws4bvlu9y1ybk RENAME TO schema_qmwm7sg64pwysx5;`
