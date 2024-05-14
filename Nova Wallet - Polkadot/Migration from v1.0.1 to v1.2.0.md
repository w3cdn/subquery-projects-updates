# Migration from v1.0.1 to v1.2.0
```
Old project: QmUSvntAvxr1kUGESMbugxxUJaGRY13JcgG1wDphs3nMeV
New project: Qmea9t8EGmHenMwAvhiYyzANYobGLNb37E6bs5QzZFxtiX
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmUSvntAvxr1kUGESMbugxxUJaGRY13JcgG1wDphs3nMeV`)

```
docker container rm -f query_qmusvntavxr1kug && docker container rm -f node_qmusvntavxr1kug
```

 2) Execute query.

```
docker exec postgres psql -U indexer_db -c "ALTER SCHEMA schema_qmusvntavxr1kug RENAME TO schema_qmea9t8egmhenmw;"

```

 3) Run new project from coordinator (`Qmea9t8EGmHenMwAvhiYyzANYobGLNb37E6bs5QzZFxtiX`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmusvntavxr1kug RENAME TO schema_qmea9t8egmhenmw;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)