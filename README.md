# TrustCat.ai – CatChain Fabric Network 🐾

This repository contains the genesis configuration and operational tooling for the **TrustCat CatChain**, a Hyperledger Fabric 2.5 network powering verifiable compute proofs for AI workloads.

## Components
- `docker-compose.yaml` — orderer + peer + couchdb network
- `configtx.yaml` — genesis and channel definitions
- `chaincode/catproof` — proof-of-compute smart contract (Go)
- `system-genesis-block/` — Fabric bootstrap block

## Quickstart
```bash
docker compose up -d
peer channel list
# trustcat-chain
