<!-- Profile README — Alejandro Saez Castells | Backend & Smart Contract Engineer -->

<h1 align="center">Alejandro Saez Castells</h1>

<p align="center">
  <strong>Backend & Smart Contract Engineer</strong><br/>
  Solidity/EVM · Java/Spring · TypeScript/Node · Production Web3 systems · Real-world workflow logic
</p>

<p align="center">
  <a href="https://www.alsaecas.dev/">
    <img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-alsaecas.dev-111111?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/alejandrosaezc/">
    <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://github.com/alsaecas">
    <img alt="GitHub" src="https://img.shields.io/badge/GitHub-alsaecas-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

---

## About

I build production-oriented backend systems, smart contracts, and Web3 integrations.

My background combines **industrial automation**, **backend engineering**, and **blockchain development**. That gives me a practical systems mindset: model the real workflow first, keep state transitions explicit, handle edge cases, and design software around reliability, permissions, timing, and failure modes.

**Current technical focus:**

* **Backend systems:** Java/Spring Boot, TypeScript/Node.js, REST APIs, PostgreSQL, authentication, OpenAPI, CI/CD
* **Smart contracts:** Solidity, Foundry, Hardhat, EVM, ERC standards, access control, state machines, testing
* **Web3 integrations:** wallets, contract interactions, tokenized workflows, on-chain/off-chain boundaries
* **Real-world workflows:** roles, permissions, deadlines, KPIs, certificates, incentives, traceability
* **Industrial systems thinking:** automation, controls, OT/IT integration, operational constraints, debugging under real-world pressure

---

## Selected engineering work

### 🏆 On-chain Flight Turnaround Checklist

Smart-contract-backed aviation workflow built during **Decode Travel Barcelona** with **Camino Network × Vueling**.
The project models aircraft turnaround operations through task ownership, completion states, SLA/deadline logic, KPI computation, certification, and ERC-721 reward badges.

**What it demonstrates:** smart contracts as state machines for real-world operational workflows.
**Focus:** Solidity · TypeScript · Camino Network · IPFS · ERC-721 · workflow state · operational process modeling
**Repo:** https://github.com/aanit-app/decode-travel-with-vueling

---

### 🎟️ Fallas Passport — ERC-1155 location-based checkpoints

Location-based NFT passport concept for Fallas in Valencia. Visitors claim checkpoint stamps by scanning QR/NFC on-site; the contract verifies EIP-712 signed vouchers instead of storing physical location data on-chain.

**What it demonstrates:** on-chain/off-chain boundary design, signed claims, replay protection, and privacy-aware presence workflows.
**Focus:** Solidity · Foundry · ERC-1155 · EIP-712 · signed vouchers · replay protection · QR/NFC flow
**Repo:** https://github.com/alsaecas/fallas-passport-1155

---

### 🔐 Fixed-Amount ERC20 Staking with ETH Rewards

Production-style staking system where users stake a fixed amount of ERC20 tokens and claim ETH rewards by period. Includes admin flows, reward funding, custom errors, events, scripts, and security-focused testing.

**What it demonstrates:** reward accounting, secure token handling, admin boundaries, and Foundry-based contract validation.
**Focus:** Solidity · Foundry · SafeERC20 · reentrancy protection · rewards · test coverage · scripts
**Repo:** https://github.com/alsaecas/erc20-staking-eth-rewards

---

### 🏦 SavingsBankPro — ETH time-locked savings

Solidity/Foundry smart contract system for multiple ETH savings plans with unlock times, early-withdraw penalties, treasury routing, pause controls, and security tests.

**What it demonstrates:** time-based contract logic, withdrawal constraints, treasury routing, and production-style safety controls.
**Focus:** Solidity · Foundry · time locks · penalties · pausable flows · reentrancy protection · fuzz testing
**Repo:** https://github.com/alsaecas/savings-bank-pro-foundry

---

### 🧾 Chain Bounty Marketplace

On-chain bounty marketplace prototype with ERC20 rewards, escrowed bounty creation, work submissions, winner selection, deadline handling, cancellation flows, and payout execution.

**What it demonstrates:** marketplace state design, escrow logic, deadline-driven flows, and clear on-chain payout rules.
**Focus:** Solidity · OpenZeppelin · ERC20 · escrow · marketplace logic · deadline-based flows
**Repo:** https://github.com/alsaecas/Chain-Bounty-Marketplace

---

## Technical stack

### Smart contracts & Web3

Solidity · Foundry · Hardhat · EVM · ERC-20 · ERC-721 · ERC-1155 · OpenZeppelin · EIP-712 · IPFS · DeFi primitives · wallet integrations

### Backend systems

Java · Spring Boot · Node.js · TypeScript · REST APIs · PostgreSQL · MongoDB · Keycloak · OpenAPI/Swagger · Docker · GitHub Actions · GitLab CI/CD

### Frontend & product

React · TypeScript · Web3 wallet flows · marketplace features · KYC/user verification flows · Web2/Web3 integrations

### Industrial background

PLCs · SCADA · OT/IT integration · automation and controls · automotive production environments · operational reliability

---

## Engineering principles

* Model the real workflow before choosing the technical design.
* Keep contract and API state transitions explicit.
* Treat authentication, wallets, providers, signatures, and external data as reliability boundaries.
* Prefer simple, testable architectures over unnecessary complexity.
* Use Web3 where it adds traceability, incentives, automation, or verifiable state — not as decoration.
* Document trade-offs clearly: assumptions, admin trust, upgrade paths, limitations, and production-hardening steps.

---

## Links

* Portfolio: https://www.alsaecas.dev/
* LinkedIn: https://www.linkedin.com/in/alejandrosaezc/
* GitHub: https://github.com/alsaecas
