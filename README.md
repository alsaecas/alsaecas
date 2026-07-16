<!-- Profile README — Alejandro Saez Castells -->

<h1 align="center">Alejandro Saez Castells</h1>

<p align="center">
  <strong>Senior Backend & Smart Contract Engineer</strong><br/>
  Production-grade Web3 systems · Java/Spring · TypeScript/Node.js · Solidity/EVM
</p>

<p align="center">
  Valencia, Spain · Open to remote opportunities across EMEA and international teams
</p>

<p align="center">
  <a href="https://www.alsaecas.dev/">
    <img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-alsaecas.dev-111111?style=for-the-badge&logo=vercel&logoColor=white" />
  </a>
  <a href="https://www.alsaecas.dev/cv">
    <img alt="CV" src="https://img.shields.io/badge/CV-View_resume-374151?style=for-the-badge&logo=readme&logoColor=white" />
  </a>
  <a href="https://www.linkedin.com/in/alejandrosaezc/">
    <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://www.alsaecas.dev/contact">
    <img alt="Contact" src="https://img.shields.io/badge/Contact-Let's_talk-7C3AED?style=for-the-badge&logo=maildotru&logoColor=white" />
  </a>
</p>

---

## About me

I build backend services, smart contracts, blockchain integrations, and workflow systems where **roles, permissions, money, state, deadlines, and reliability matter**.

My background spans more than 15 years of engineering, from industrial automation and operational systems to backend, full-stack, and blockchain development. I bring the same mindset to software that production environments demand: explicit state, controlled failure modes, observable operations, strong testing, and designs that remain understandable under pressure.

My current focus is the intersection of:

- **Backend and identity systems** — APIs, authentication, federation, persistence, integrations, and CI/CD
- **Smart contracts and protocol integrations** — permissions, state machines, DeFi routers, token flows, deadlines, and security boundaries
- **Programmable payments** — agent spending policies, payment intents, wallets, receipts, and authorization rules
- **Real-world workflows** — aviation, travel, marketplaces, team finance, identity, and operational automation

---

## Featured engineering work

### ⚡ CSPR AgentPay Guard

**Policy-controlled HTTP 402 payments for autonomous AI agents.**

An agentic-payment system where an autonomous agent can purchase a protected API response only when a deterministic spending policy authorizes it. Payments are bound to exact requests and protected through merchant allowlists, spending limits, expiration checks, audit events, and replay prevention.

The project includes a TypeScript monorepo, protected API, policy engine, agent runner, dashboard, Casper adapter, and an Odra smart contract for recording proof data on Casper Testnet.

**Demonstrates:** agentic commerce · HTTP 402 · policy engines · request-bound receipts · replay protection · Casper Testnet · on-chain proof recording

**Stack:** TypeScript · Node.js · Next.js · Rust · Odra · Casper · Vitest

[Live demo](https://cspr-agentpay-guard.vercel.app/) · [Source code](https://github.com/alsaecas/cspr-agentpay-guard) · [DoraHacks submission](https://dorahacks.io/buidl/46706)

---

### 🏦 CupTreasury

**A self-custodial treasury for football teams, squads, and fan groups.**

CupTreasury replaces contribution reminders and expense approvals managed through WhatsApp with a structured treasury workflow. Captain and Treasurer approvals are transformed into exact, one-time payment capabilities that can be evaluated through Tether WDK policies.

The project includes contribution tracking, match-day expense requests, role-based approvals, PaymentIntent authorization, WDK policy simulation, safe no-broadcast signing, proof artifacts, automated tests, and a judge-facing verification flow.

**Demonstrates:** programmable payments · self-custody · approval policies · capability-based authorization · Tether WDK · security boundaries

**Stack:** Next.js · TypeScript · Tether WDK · React · Vitest · GitHub Actions

[Live demo](https://cuptreasury.vercel.app/) · [Source code](https://github.com/alsaecas/cuptreasury)

---

### 🔄 SwapGuard

**A security-aware Uniswap V2 integration with slippage protection and reproducible fork testing.**

SwapGuard demonstrates the complete ERC-20 swap lifecycle: router quotations, exact-input swaps, minimum-output protection, transaction deadlines, temporary router allowances, direct output delivery, and transaction receipt handling.

The project includes a focused Solidity integration contract, behavioral mocks, unit and fuzz tests, pinned Arbitrum fork tests against real deployed contracts, local Anvil tooling, CI, and a React interface built with wagmi and viem.

The public deployment is an interactive portfolio preview. Real swap execution is available through the reproducible local Arbitrum fork without using real funds.

**Demonstrates:** DeFi integration · Uniswap V2 · ERC-20 allowances · slippage protection · router trust boundaries · fork testing · wallet transaction UX

**Stack:** Solidity · Foundry · OpenZeppelin · React · TypeScript · wagmi · viem · Arbitrum · Vercel

[Interactive demo](https://swapguard-zeta.vercel.app/) · [Source code](https://github.com/alsaecas/swapguard)

---

### ✈️ On-chain Flight Turnaround Checklist

**Winner of the Blockchain-based Turnaround Checklist challenge at Decode Travel Barcelona 2025.**

A smart-contract-backed aviation workflow created with Camino Network and Vueling. Each aircraft turnaround is modeled through task ownership, role permissions, completion states, operational deadlines, SLA and KPI computation, certification, and ERC-721 reward badges.

The project translates a real multi-actor operational process into explicit, auditable smart-contract state transitions.

**Demonstrates:** operational workflow modeling · smart-contract state machines · deadlines · KPIs · certification · tokenized incentives

**Stack:** Solidity · TypeScript · Next.js · Camino Network · IPFS · ERC-721

[Case study](https://www.alsaecas.dev/projects/turnaround-checklist-dapp) · [Source code](https://github.com/aanit-app/decode-travel-with-vueling)

---

### 🧰 Fondant

**A Ganache-like local development environment for Casper applications.**

Fondant packages Casper CCTL functionality into a Docker-based application suite with interfaces for accounts, blocks, deploys, events, logs, and local RPC workflows.

It was designed to shorten the feedback loop for developers building and testing Casper smart contracts without relying entirely on shared networks.

**Demonstrates:** blockchain developer tooling · local infrastructure · Dockerized environments · RPC integration · developer experience

**Stack:** TypeScript · Rust · Docker · Docker Compose · CCTL · Casper

[Case study](https://www.alsaecas.dev/projects/fondant) · [Source code](https://github.com/defdone/fondant-app)

---

## Production backend engineering

Alongside my public Web3 work, I build backend and identity systems using **Java, Spring Boot, PostgreSQL, Keycloak, REST APIs, OpenAPI, Docker, Gradle, and CI/CD**.

My professional work includes:

- Identity federation, SSO, authentication flows, and role synchronization
- Keycloak extensions, authenticators, event listeners, and client policies
- REST and gRPC service design
- Database modeling and Flyway migrations
- External provider and blockchain integrations
- Authorization and account lifecycle rules
- Automated unit and integration testing
- Production debugging, system upgrades, and deployment workflows

---

## Technical focus

| Area | Technologies |
|---|---|
| **Backend systems** | Java, Spring Boot, Node.js, TypeScript, REST, gRPC, PostgreSQL, MongoDB, OpenAPI |
| **Identity and security** | Keycloak, SSO, OAuth2, role-based access control, federation, policy enforcement |
| **Smart contracts** | Solidity, Foundry, Hardhat, OpenZeppelin, EVM, ERC-20, ERC-721, ERC-1155, EIP-712 |
| **DeFi and payments** | Uniswap V2 integrations, token allowances, slippage, fork testing, Tether WDK, payment policies |
| **Blockchain ecosystems** | Ethereum/EVM, Arbitrum, Camino Network, Casper, wallets, IPFS |
| **Infrastructure** | Docker, GitHub Actions, GitLab CI/CD, Gradle, Vercel, AWS services |
| **Frontend and product** | React, Next.js, wagmi, viem, wallet flows, dashboards, marketplaces, KYC integrations |
| **Industrial systems** | PLCs, SCADA, automation, controls, OT/IT integration, automotive production |

---

## More Solidity and EVM work

<details>
<summary><strong>View additional smart-contract projects</strong></summary>

<br/>

### Fallas Passport

Location-based ERC-1155 passport using EIP-712 signed vouchers, QR/NFC checkpoints, replay protection, and privacy-aware presence verification.

[View repository](https://github.com/alsaecas/fallas-passport-1155)

### Fixed-Amount ERC20 Staking

Fixed-token staking system with period-based ETH rewards, SafeERC20 handling, custom errors, admin boundaries, and security-focused Foundry tests.

[View repository](https://github.com/alsaecas/erc20-staking-eth-rewards)

### SavingsBankPro

Time-locked ETH savings plans with early-withdraw penalties, treasury routing, pause controls, reentrancy protection, and fuzz testing.

[View repository](https://github.com/alsaecas/savings-bank-pro-foundry)

### Chain Bounty Marketplace

ERC-20-funded bounty marketplace with escrow, submissions, deadlines, winner selection, cancellation rules, and payout execution.

[View repository](https://github.com/alsaecas/Chain-Bounty-Marketplace)

</details>

---

## How I approach engineering

- Start with the actors, rules, constraints, and failure modes—not the framework.
- Keep contract and API state transitions explicit and testable.
- Treat authentication, wallets, signatures, providers, tokens, and external protocols as reliability boundaries.
- Separate demonstrable functionality from assumptions, simulations, and future production work.
- Use blockchain where it provides verifiable state, traceability, programmable authorization, or meaningful automation.
- Test isolated behavior with mocks and external integrations against reproducible environments.
- Document architecture, trade-offs, trust assumptions, limitations, and production-hardening requirements.

---

## Currently exploring

- Autonomous-agent payments and HTTP 402 workflows
- Policy-controlled wallets and programmable payment authorization
- DeFi protocol integrations and secure token flows
- Reproducible mainnet-fork testing
- On-chain proof and audit systems
- Blockchain-backed operational workflows
- Backend and identity infrastructure for Web3 products

---

## Let’s connect

I am open to remote opportunities involving **senior backend engineering, smart contracts, DeFi integrations, blockchain platforms, Web3 infrastructure, programmable payments, and technically ambitious product development**.

[Portfolio](https://www.alsaecas.dev/) · [LinkedIn](https://www.linkedin.com/in/alejandrosaezc/) · [Contact](https://www.alsaecas.dev/contact)
