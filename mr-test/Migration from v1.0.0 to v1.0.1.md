# Migration from v1.0.0 to v1.0.1
```
Old project: QmeuYH4K7QAu8ZkMM7iVNDYPKVMfTn7bpPom5uJWSusfDJ
New project: QmUJmKFita7WQr3PV7P8HDqDuFgDHTpqGyzT55NoYXudCX
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmeuYH4K7QAu8ZkMM7iVNDYPKVMfTn7bpPom5uJWSusfDJ`)

```
docker container rm -f query_qmeuyh4k7qau8zk && docker container rm -f node_qmeuyh4k7qau8zk
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmeuyh4k7qau8zk RENAME TO schema_qmujmkfita7wqr3;"

```

 3) Run new project from coordinator (`QmUJmKFita7WQr3PV7P8HDqDuFgDHTpqGyzT55NoYXudCX`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmeuyh4k7qau8zk RENAME TO schema_qmujmkfita7wqr3;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_bot](https://t.me/subquery_eagle_eye_bot)
