<!-- GitHub Profile README — Alejandro Saez Castells -->

<h1 align="center">Alejandro Saez Castells</h1>

<p align="center">
  <strong>Senior Backend & Smart Contract Engineer</strong><br/>
  Production systems · Protocol engineering · Identity & security · Programmable payments
</p>

<p align="center">
  Valencia, Spain · Remote-first · EMEA & international teams
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

## Engineering profile

I build software where **state, permissions, money, identity, deadlines, and failure modes matter**.

My background spans more than 15 years of engineering, from industrial automation and operational systems to backend, full-stack, mobile, and blockchain development. That path shaped how I approach software today: model the real rules first, keep state transitions explicit, constrain privilege, design for failure, and prove important behaviour with tests rather than assumptions.

My work now sits mainly at the intersection of:

- **Backend & identity systems** — Kotlin, Java, Spring Boot, PostgreSQL, Keycloak, OAuth2/OIDC, APIs, messaging, integrations, CI/CD
- **Smart contracts & protocol engineering** — Solidity, EVM, signed intents, state machines, token flows, escrow, vesting, replay protection, security boundaries
- **DeFi & programmable payments** — allowances, settlement, pricing, oracle normalization, payment policies, self-custody and request-bound authorization
- **Production product engineering** — React Native, React/Next.js, TypeScript, mobile marketplaces, operational workflows and release delivery

> I care less about adding blockchain to a product than about using it where verifiable state, programmable authorization, settlement, traceability, or shared trust genuinely improves the system.

---

# Featured engineering work

These projects show three different sides of my engineering profile: **production delivery**, **protocol/security depth**, and **end-to-end Web3 execution**.

| Project | Primary signal | Highlights |
| --- | --- | --- |
| **[OrderForge](https://github.com/alsaecas/orderforge)** | Protocol & smart-contract security | EIP-712 · ERC-1271 · partial fills · replay protection · fuzzing · stateful invariants |
| **[LaunchProof](https://github.com/alsaecas/launchproof)** | End-to-end Web3 engineering | token sale · escrow · refunds · vesting · oracles · Sepolia deployment · frontend |
| **[Cooking](https://www.alsaecas.dev/projects/cooking)** | Production product engineering | real marketplace · Android/iOS · kitchen operations · state management · release delivery |

---

## ⚒️ OrderForge

**Non-custodial EIP-712 signed limit-order settlement with partial fills, ERC-1271 and stateful Foundry invariants.**

OrderForge is a security-focused Solidity reference protocol for off-chain signed orders and on-chain settlement. A maker signs an EIP-712 order; a taker can settle all or part of it without the protocol taking custody of funds.

The design covers the areas where signed-order protocols become interesting: domain separation, contract-wallet signatures, replay protection, nonce binding, cancellation, expiry, restricted takers, exact cumulative settlement and token-transfer failure semantics.

### What the protocol demonstrates

- **EIP-712 structured signing** bound to chain ID and verifying contract
- **EOA + ERC-1271 signature verification** through OpenZeppelin `SignatureChecker`
- **Nonce binding and invalidation** to prevent conflicting signed orders sharing lifecycle state
- **Per-order cancellation, expiry and optional taker restriction**
- **Non-custodial settlement** using direct `SafeERC20` transfers and reentrancy protection
- **Cumulative partial-fill accounting** that reaches the exact signed buy amount at completion
- Explicit ABI/hashing examples with `abi.encode`, `abi.decode`, `abi.encodeCall`, `abi.encodePacked` and `keccak256`

### Verified engineering baseline

**44 Forge tests** · **35 unit** · **4 fuzz properties** · **5 stateful invariants**  
**4,096 fuzz runs/property** · **65,536 calls/invariant** · **100% production-contract line/statement/branch/function coverage**  
**Slither: 0 results after documented narrow exclusions** · protected `main` · stable **v1.0.0** release

The adversarial suite covers mutated and malformed signatures, cross-chain replay, ERC-1271 rejection, false-returning ERC-20 rollback, overfill protection, partial-fill exactness and terminal lifecycle states.

**Stack:** Solidity · Foundry · OpenZeppelin · Slither · GitHub Actions

[Source code](https://github.com/alsaecas/orderforge) · [v1.0.0 release](https://github.com/alsaecas/orderforge/releases/tag/v1.0.0) · [Architecture](https://github.com/alsaecas/orderforge/blob/main/docs/ARCHITECTURE.md) · [Threat model](https://github.com/alsaecas/orderforge/blob/main/docs/THREAT-MODEL.md) · [Testing strategy](https://github.com/alsaecas/orderforge/blob/main/docs/TESTING.md)

> Educational/reference software. OrderForge has not undergone a professional smart-contract security audit and is not presented as production-ready financial infrastructure.

---

## 🚀 LaunchProof

**A transparent token-sale protocol with verifiable pricing, escrowed contributions, exact-asset refunds, and vesting.**

LaunchProof is a full-stack Ethereum token-presale reference implementation built around a non-upgradeable Solidity protocol, deterministic deployment scripts, comprehensive Foundry testing, and a Next.js application that communicates directly with the blockchain.

The protocol supports ordered sale phases, native ETH and ERC-20 payments, Chainlink-compatible price feeds, purchase-time USD accounting, soft-cap finalization, cancellation, refunds in the original contributed asset, TGE unlocks, cliffs, linear vesting and liability-aware recovery rules.

The live V2 demonstration is deployed on **Ethereum Sepolia** with a fixed supply of **30,000,000 LPF**, capped demonstration stablecoins, immutable demo feeds and a rate-limited faucet. The complete purchase path has been exercised on-chain from faucet claim through approval, purchase and LPF delivery.

**Validation:** 31/31 Foundry tests · 8/8 frontend tests · unit, fuzz, reentrancy, oracle-failure, lifecycle, vesting, recovery and stateful invariant coverage

**Demonstrates:** protocol architecture · escrow · refunds · phased pricing · oracle normalization · vesting · role boundaries · deterministic deployments · on-chain verification · Web3 UX

**Stack:** Solidity · Foundry · OpenZeppelin · Chainlink interfaces · Next.js · React · TypeScript · wagmi · viem · RainbowKit · Ethereum Sepolia · Vercel

[Live application](https://launchproof-app.vercel.app/) · [Source code](https://github.com/alsaecas/launchproof) · [Sepolia deployment](https://sepolia.etherscan.io/address/0x1435ab5b973f92b4be10abd096f7dd80ff1354e4)

> Educational reference implementation. The contracts have not been professionally audited and are not presented as production-ready financial infrastructure.

---

## 🍳 Cooking

**A production mobile marketplace connecting customers with nearby local kitchens.**

Cooking is a two-sided product composed of Android and iOS customer applications and a dedicated Android manager application used by kitchens in day-to-day operations.

I contribute across customer flows, store operations and supporting API behaviour: marketplace discovery, maps, menus, favourites, cart state, authentication, sharing, ordering, kitchen workflows, notifications, product availability, automated testing, release configuration and production troubleshooting.

What makes the project valuable from an engineering perspective is not a single framework; it is maintaining coherent state across customers and kitchens while handling platform-specific behaviour, native dependencies, asynchronous data, operational failure modes and app-store delivery.

**Demonstrates:** production software · two-sided marketplaces · cross-platform reliability · operational workflows · state management · automated mobile testing · release engineering

**Stack:** React Native · Expo · TypeScript · Expo Router · TanStack Query · Jotai · Supabase · EAS Build · Jest · Maestro

[Case study](https://www.alsaecas.dev/projects/cooking) · [Product website](https://www.cookingpro.es/) · [Google Play](https://play.google.com/store/apps/details?id=com.cooking.marketplaceapp) · [App Store](https://apps.apple.com/es/app/cooking-comida-casera/id6753148870)

---

# Selected blockchain & product work

## 🔄 SwapGuard

**Security-aware Uniswap V2 integration with slippage protection and reproducible fork testing.**

A focused Solidity + React project covering router quotations, exact-input swaps, minimum-output protection, deadlines, temporary allowances, receipt handling, behavioural mocks and pinned Arbitrum fork tests against deployed contracts.

**Stack:** Solidity · Foundry · OpenZeppelin · React · TypeScript · wagmi · viem · Arbitrum · Anvil

[Interactive demo](https://swapguard-zeta.vercel.app/) · [Source](https://github.com/alsaecas/swapguard)

### ⚡ CSPR AgentPay Guard

**Policy-controlled HTTP 402 payments for autonomous AI agents.**

Request-bound payment authorization with merchant allowlists, spending limits, expiration, revocation, replay prevention, audit events and Casper Testnet proof recording.

**Stack:** TypeScript · Node.js · Next.js · Rust · Odra · Casper · Vitest

[Live demo](https://cspr-agentpay-guard.vercel.app/) · [Source](https://github.com/alsaecas/cspr-agentpay-guard) · [DoraHacks](https://dorahacks.io/buidl/46706)

### 🏦 CupTreasury

**Self-custodial treasury workflows for teams, squads and fan groups.**

Turns contribution and expense approvals into exact, one-time payment capabilities evaluated through policy rules, with role-based approval, PaymentIntent authorization, WDK simulation and safe no-broadcast signing.

**Stack:** Next.js · TypeScript · Tether WDK · React · Vitest · GitHub Actions

[Live demo](https://cuptreasury.vercel.app/) · [Source](https://github.com/alsaecas/cuptreasury) · [DoraHacks](https://dorahacks.io/buidl/46738)

### ✈️ On-chain Flight Turnaround Checklist

**Winner of the Blockchain-based Turnaround Checklist challenge at Decode Travel Barcelona 2025.**

A Camino Network / Vueling aviation workflow modelling task ownership, role permissions, operational deadlines, SLA/KPI computation, certification and ERC-721 reward badges as explicit smart-contract state transitions.

**Stack:** Solidity · TypeScript · Next.js · Camino Network · IPFS · ERC-721

[Case study](https://www.alsaecas.dev/projects/turnaround-checklist-dapp) · [Source](https://github.com/aanit-app/decode-travel-with-vueling)

### 🧰 Fondant

**A Ganache-like local development environment for Casper applications.**

Docker-based tooling around Casper CCTL with interfaces for accounts, blocks, deploys, events, logs and local RPC workflows, designed to shorten the smart-contract development feedback loop.

**Stack:** TypeScript · Rust · Docker · Docker Compose · CCTL · Casper

[Case study](https://www.alsaecas.dev/projects/fondant) · [Source](https://github.com/defdone/fondant-app)

---

# Production backend & identity engineering

Alongside public blockchain and product work, I build backend and identity systems with **Kotlin, Java, Spring Boot, PostgreSQL, Keycloak, REST/OpenAPI, Docker, Gradle and CI/CD**.

Representative engineering areas include:

- Identity federation, SSO, OAuth2/OIDC and role synchronization
- Custom Keycloak authenticators, event listeners, storage providers and client policies
- REST and gRPC service design
- PostgreSQL modelling and Flyway migrations
- Authorization and account-lifecycle rules
- External provider and blockchain integrations
- Background messaging and asynchronous processing
- Unit, integration and controller testing
- Production debugging, dependency upgrades, migrations and release workflows

---

# Technical toolkit

| Area | Technologies & concepts |
| --- | --- |
| **Backend** | Kotlin · Java · Spring Boot · Node.js · TypeScript · REST · gRPC · PostgreSQL · MongoDB · OpenAPI |
| **Identity & security** | Keycloak · OAuth2 · OpenID Connect · SSO · federation · RBAC · policy enforcement |
| **Smart contracts** | Solidity · Foundry · Hardhat · OpenZeppelin · EVM · EIP-712 · ERC-1271 · ERC-20/721/1155 |
| **Protocol testing** | Unit tests · fuzzing · stateful invariants · behavioural mocks · fork tests · reentrancy tests · Slither |
| **DeFi & payments** | signed intents · settlement · Uniswap V2 · allowances · slippage · Chainlink-compatible feeds · payment policies |
| **Web3 application** | React · Next.js · TypeScript · wagmi · viem · RainbowKit · wallet flows · transaction UX |
| **Mobile** | React Native · Expo · Android · iOS · TanStack Query · Jotai · EAS Build · Jest · Maestro |
| **Infrastructure** | Docker · Docker Compose · GitHub Actions · GitLab CI/CD · Gradle · Vercel · AWS services |
| **Industrial systems** | PLCs · SCADA · controls · automation · OT/IT integration · automotive production |

---

# More Solidity & EVM work

<details>
<summary><strong>Additional smart-contract projects</strong></summary>

<br/>

**Fallas Passport** — Location-based ERC-1155 passport using EIP-712 signed vouchers, QR/NFC checkpoints, replay protection and privacy-aware presence verification.  
[Repository](https://github.com/alsaecas/fallas-passport-1155)

**Fixed-Amount ERC-20 Staking** — Fixed-token staking with period-based ETH rewards, `SafeERC20`, custom errors, administrative boundaries and security-focused Foundry tests.  
[Repository](https://github.com/alsaecas/erc20-staking-eth-rewards)

**SavingsBankPro** — Time-locked ETH savings plans with early-withdrawal penalties, treasury routing, pause controls, reentrancy protection and fuzz testing.  
[Repository](https://github.com/alsaecas/savings-bank-pro-foundry)

**Chain Bounty Marketplace** — ERC-20-funded bounty marketplace with escrow, submissions, deadlines, winner selection, cancellation rules and payout execution.  
[Repository](https://github.com/alsaecas/Chain-Bounty-Marketplace)

</details>

---

# How I approach engineering

1. **Model the domain before the framework.** Start with actors, assets, permissions, invariants, deadlines and failure modes.
2. **Make state transitions explicit.** Contract, API, database and UI states should be understandable and testable.
3. **Treat trust boundaries as first-class design inputs.** Signatures, tokens, wallets, identity providers, oracles and external APIs can fail or behave unexpectedly.
4. **Prefer least privilege and narrow capabilities.** Administrative power should exist only where the system genuinely requires it.
5. **Preserve liabilities during failure.** Refunds, claims, escrowed balances and outstanding obligations must survive cancellation and recovery paths.
6. **Test properties, not only examples.** Unit tests explain behaviour; fuzzing and invariants challenge assumptions across larger state spaces.
7. **Document what the system does not guarantee.** Limitations, unsupported token behaviour, deployment status and audit status should be explicit.
8. **Keep architecture understandable under pressure.** Security and reliability improve when the state model can still be reasoned about during incidents and changes.

---

## Currently exploring

- Signed intents, settlement and replay-safe authorization
- Stateful invariant testing and adversarial smart-contract verification
- Secure token distribution, escrow, refunds and vesting
- Programmable payment policies and autonomous-agent commerce
- DeFi integrations and reproducible fork environments
- Identity federation and policy-driven authorization
- Blockchain-backed operational workflows where shared verifiability has real value

---

<p align="center">
  <strong>Backend systems. Smart contracts. Identity. Payments. Production software.</strong>
</p>

<p align="center">
  <a href="https://www.alsaecas.dev/">Portfolio</a> ·
  <a href="https://www.alsaecas.dev/cv">CV</a> ·
  <a href="https://www.linkedin.com/in/alejandrosaezc/">LinkedIn</a> ·
  <a href="https://www.alsaecas.dev/contact">Contact</a>
</p>
