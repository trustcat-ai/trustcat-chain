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
# 🐾 TrustCat.ai — CatChain Fabric Genesis

**Network Launch:** 2025-10-19  
**Fabric Version:** v2.5  
**Orderer:** trustcat.ai  
**Peer:** mineai.trustcat.ai  
**Channel:** `catchain`  
**Genesis Block:** Block 0  
**Timestamp:** (pending fetch)
**Hash (SHA256):** (pending)

---

### 🧱 Onboarding a New Node (Provider/Broker)
```bash
git clone git@github.com:trustcat-ai/trustcat-chain.git
cd trustcat-chain
export PATH=$PATH:$HOME/fabric/fabric-samples/bin
./scripts/join_peer.sh mineai.trustcat.ai
