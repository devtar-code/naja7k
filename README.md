<img width="400" height="400" alt="image" src="https://github.com/user-attachments/assets/6435155f-e4d1-40dd-9e92-2689e10fdcdd" />


# Naja7k - AI Growth DAO – Deployment Roadmap & Architecture

## Overview
Naja7k AI Growth DAO is an autonomous organization integrating AI agents into a DAO governance model. 
It is funded with Bitcoin (BTC) via tBTC/WBTC or sBTC, and runs on EVM L2 infrastructure with strict treasury policies.

The system is designed to begin with **AI agents in proposal-only mode**, gradually moving towards **capped autonomous execution** with strong security and transparency controls.

---

<img width="5370" height="2970" alt="AI_Growth_DAO_Enterprise_Architecture" src="https://github.com/user-attachments/assets/f1b1ec85-3216-479e-a5a2-91665b000ddf" />

## Architecture Summary

**Layers:**
1. **User/Community Layer:** Token holders interact via Web3 wallets and a front-end dApp.
2. **Governance Layer:** Off-chain Snapshot voting and on-chain governance via OZ Governor or Aragon OSx.
3. **Execution Layer:** Safe Treasury (multisig), SafeSnap module, and Zodiac Roles for permissions/spend caps.
4. **AI Agents Layer:** MarketingAgent, SalesAgent, and future OpsAgent (AutoGen/CrewAI-based) propose initiatives and budgets.
5. **Integration Layer:** API Gateway, Chainlink Functions (data feeds), Gelato Automate (scheduling), UMA/Reality.eth (assertions/disputes).
6. **Funding & Settlement Layer:** BTC reserves, bridges (tBTC/WBTC), optional Stacks sBTC path, and streaming payments via Sablier/Superfluid.

---

## 12-Week Deployment Roadmap

### **Sprint 1: Foundation (Weeks 1–2)**
- Repo setup + CI tests
- Deploy Safe (testnet) and ERC-20 governance token
- Create Snapshot space (testnet)
- Author DAO Charter v1
- Scaffold API Gateway (FastAPI/Node)

### **Sprint 2: Governance & Treasury (Weeks 3–4)**
- Install SafeSnap on Safe (testnet)
- Connect Snapshot → SafeSnap
- Add Zodiac Roles for spend caps
- Simulate BTC→tBTC funding
- Hardware wallet setup for signers

### **Sprint 3: Agents MVP (Weeks 5–6)**
- Deploy MarketingAgent and SalesAgent
- Integrate with API Gateway (mock data)
- Weekly KPI proposal job (Gelato)
- Chainlink Functions mock

### **Sprint 4: Data & Oracles (Weeks 7–8)**
- Connect real CRM/ad accounts
- Chainlink Functions integration
- UMA/Reality KPI assertions
- Telemetry (OpenTelemetry + Grafana)
- Security review #1

### **Sprint 5: BTC Funding & Payments (Weeks 9–10)**
- Mainnet BTC→tBTC bridge
- Treasury reserve policy
- Stream founder stipend (Sablier/Superfluid)
- Coordinape rewards pilot
- Security review #2

### **Sprint 6: Limited Autonomy Pilot (Weeks 11–12)**
- Enable auto-exec within Roles caps
- Runbooks + incident playbooks
- Audit prep
- Public launch checklist

---

## Security Controls
- BTC core reserve un-bridged; only working capital on L2
- Strict Roles allowlists; no arbitrary exec for agents
- 2-of-3 Safe signers with hardware wallets
- Tx alerts, spend-cap alerts, and KPI anomaly checks

---

## Key Repositories & Modules
- `/contracts` → Governance token, SafeSnap config, Roles module
- `/agents` → AI agent code (AutoGen/CrewAI)
- `/gateway` → API Gateway (FastAPI/Node)
- `/infra` → Terraform/Ansible infra scripts
- `/docs` → Architecture diagrams, roadmap, runbooks

---

## References
- [Safe](https://safe.global)
- [Snapshot](https://snapshot.org)
- [Zodiac Roles](https://zodiac.wiki)
- [Chainlink Functions](https://chain.link/functions)
- [UMA](https://uma.xyz)
- [Gelato Automate](https://www.gelato.network/automate)
- [Sablier](https://sablier.com)
- [Superfluid](https://www.superfluid.finance)
