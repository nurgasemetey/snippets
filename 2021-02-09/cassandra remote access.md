### cassandra remote access







```
Make these changes in the cassandra.yaml config file:

start_rpc: true

rpc_address: 0.0.0.0

broadcast_rpc_address: \[node-ip\]

listen_address: \[node-ip\]

seed_provider:
  - class_name: ...
    - seeds: "[node-ip]"
```
