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
# 🐾 TrustCat.ai — CatChain Genesis Ledger

**Genesis Block (Block 0)**  
- **Channel ID:** system-channel  
- **Timestamp:** 2025-10-19T01:32:10Z  
- **Transaction Hash:** 73aad608a1d036abad38192f78aeecdfd88e293b4eca9341e963e3c1403833e1  
- **Orderer:** orderer.trustcat.ai:7050  
- **Org MSP:** MineAIMSP  
- **Framework:** Hyperledger Fabric v2.5  
- **Purpose:** Proof-of-Compute & AI Workload Brokerage (TrustCat Protocol Layer 0)

---

## ⚙️ Provider Onboarding (GPU Node)

```bash
curl -sSL https://raw.githubusercontent.com/trustcat-ai/trustcat-chain/main/scripts/onboard-provider.sh | bash
