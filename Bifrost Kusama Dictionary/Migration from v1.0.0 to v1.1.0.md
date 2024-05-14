# Migration from v1.0.0 to v1.1.0
```
Old project: QmUWd1o3BJb5qSR1ZaAhSw1duVgQ5bsczdfRNakNUL5cJy
New project: QmcvcN4gZkiB2JkmK6BdHh7Wzy8Gfp8R7ZHSgGajbGv6Wy
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUWd1o3BJb5qSR1ZaAhSw1duVgQ5bsczdfRNakNUL5cJy`)

```
docker container rm -f query_qmuwd1o3bjb5qsr && docker container rm -f node_qmuwd1o3bjb5qsr
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmuwd1o3bjb5qsr RENAME TO schema_qmcvcn4gzkib2jk;"

```

 3) Run new project from coordinator (`QmcvcN4gZkiB2JkmK6BdHh7Wzy8Gfp8R7ZHSgGajbGv6Wy`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmuwd1o3bjb5qsr RENAME TO schema_qmcvcn4gzkib2jk;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)