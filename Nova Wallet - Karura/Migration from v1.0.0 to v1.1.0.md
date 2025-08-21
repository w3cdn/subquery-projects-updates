# Migration from v1.0.0 to v1.1.0
```
Old project: QmTAMaR4j1JBXPNaWhTf3tj5ccAW4wLh2zxrgKhqt4ZDJ5
New project: QmS4azuhvLmCfjRs4ZA5qK9QTCi4TGPqVoQWc9oF6MGSjJ
```


## Upgrade instructions
 1) Stop old project from coordinator (`QmTAMaR4j1JBXPNaWhTf3tj5ccAW4wLh2zxrgKhqt4ZDJ5`)

```
docker container rm -f query_qmtamar4j1jbxpn && docker container rm -f node_qmtamar4j1jbxpn
```

 2) Execute query.

```
docker exec indexer_db psql -U postgres -c "ALTER SCHEMA schema_qmtamar4j1jbxpn RENAME TO schema_qms4azuhvlmcfjr;"

```

 3) Run new project from coordinator (`QmS4azuhvLmCfjRs4ZA5qK9QTCi4TGPqVoQWc9oF6MGSjJ`)

#### RAW Upgrade command. For Native requests.
`ALTER SCHEMA schema_qmtamar4j1jbxpn RENAME TO schema_qms4azuhvlmcfjr;`


___
### Setup your own indexer:

[https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md](https://github.com/web3cdnservices/subquery-indexer-toolkit/blob/mainnet/README.md)

### Projects Updates Alerts channel:

[https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD](https://github.com/web3cdnservices/subquery-projects-updates/blob/master/README.MD)

### Subquery Indexers Monitoring:

[https://t.me/subquery_eagle_eye_reserve_bot](https://t.me/subquery_eagle_eye_reserve_bot)
