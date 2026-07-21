<!-- GitHub Profile README — Alejandro Saez Castells -->

<h1 align="center">Alejandro Saez Castells</h1>

<p align="center">
  <strong>Senior Backend & Smart Contract Engineer</strong><br/>
  Production backend systems · Ethereum and Web3 protocols · Identity and security · Cross-platform product engineering
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

I build backend services, smart contracts, blockchain integrations, identity systems, and production applications where **roles, permissions, money, state, deadlines, and reliability matter**.

My background spans more than 15 years of engineering, from industrial automation and operational systems to backend, full-stack, mobile, and blockchain development.

I bring the same mindset to software that production environments demand: explicit state, controlled failure modes, observable operations, strong testing, and architectures that remain understandable under pressure.

My current focus is the intersection of:

* **Backend and identity systems** — APIs, authentication, federation, persistence, authorization, integrations, and CI/CD
* **Smart contracts and protocol engineering** — permissions, state machines, escrow, vesting, token flows, oracles, deadlines, and security boundaries
* **DeFi and programmable payments** — protocol integrations, payment intents, spending policies, wallets, receipts, and authorization rules
* **Production product engineering** — cross-platform applications, marketplaces, operational interfaces, automated testing, and release delivery
* **Real-world workflows** — aviation, travel, food marketplaces, team finance, identity, token distribution, and operational automation

---

## Featured engineering work

### 🚀 LaunchProof

**A transparent token-sale protocol with verifiable pricing, escrowed contributions, exact-asset refunds, and vesting.**

LaunchProof is a full-stack Ethereum token-presale reference implementation built around a non-upgradeable Solidity protocol, deterministic deployment scripts, comprehensive Foundry testing, and a Next.js interface that communicates directly with the blockchain.

The protocol supports ordered sale phases with time- and allocation-based transitions, multi-phase quotations, native ETH and ERC-20 payments, Chainlink-compatible price feeds, purchase-time USD accounting, soft-cap finalization, cancellation, refunds in the original contributed asset, TGE unlocks, cliffs, and linear vesting.

Contributions remain escrowed until the sale succeeds. Failed or cancelled sales preserve participant refund rights, while liability-aware recovery rules prevent administrators from withdrawing assets required for refunds or outstanding token claims.

The live V2 deployment runs on Ethereum Sepolia and is fully funded with a fixed supply of **30,000,000 LPF**. It includes capped dUSDC and dUSDT demonstration assets, immutable demo price feeds, and a rate-limited faucet with a 24-hour cooldown.

The complete purchase flow has been demonstrated on-chain: faucet claim, exact token approval, stablecoin purchase, and LPF delivery.

**Validation:** 31/31 Foundry tests · 8/8 frontend tests · unit, fuzz, reentrancy, oracle-failure, lifecycle, vesting, recovery, and stateful invariant coverage

**Demonstrates:** token-sale architecture · escrow · exact-asset refunds · phased pricing · Chainlink-compatible oracles · stablecoin decimal normalization · vesting · role-based security · invariant testing · deterministic deployments · on-chain verification

**Stack:** Solidity · Foundry · OpenZeppelin · Chainlink interfaces · Next.js · React · TypeScript · wagmi · viem · RainbowKit · Ethereum Sepolia · Vercel

[Live application](https://launchproof-app.vercel.app/) · [Source code](https://github.com/alsaecas/launchproof) · [Sepolia deployment](https://sepolia.etherscan.io/address/0x1435ab5b973f92b4be10abd096f7dd80ff1354e4)

> Educational reference implementation. The contracts have not been professionally audited and are not presented as production-ready financial infrastructure.

---

### 🍳 Cooking

**A production mobile marketplace connecting customers with nearby local kitchens.**

Cooking is a two-sided product composed of Android and iOS customer applications and a dedicated Android manager application used by kitchens for daily operations.

I contribute across the customer application, the store-facing manager experience, and supporting API behaviour. My work includes marketplace discovery, maps, menus, favourites, cart state, authentication, sharing, order UX, store order workflows, notifications, product availability, automated testing, release configuration, and production troubleshooting.

The project requires maintaining consistent product state across customer and kitchen workflows while handling Android- and iOS-specific behaviour, mobile failure states, native dependencies, and app-store delivery.

**Demonstrates:** production mobile engineering · two-sided marketplaces · cross-platform reliability · operational software · state management · automated mobile testing · release readiness

**Stack:** React Native · Expo · TypeScript · Expo Router · TanStack Query · Jotai · Supabase · EAS Build · Jest · Maestro

[Case study](https://www.alsaecas.dev/projects/cooking) · [Product website](https://www.cookingpro.es/) · [Customer app · Google Play](https://play.google.com/store/apps/details?id=com.cooking.marketplaceapp) · [Customer app · App Store](https://apps.apple.com/es/app/cooking-comida-casera/id6753148870)

---

### ⚡ CSPR AgentPay Guard

**Policy-controlled HTTP 402 payments for autonomous AI agents.**

CSPR AgentPay Guard is an agentic-payment system where an autonomous agent can purchase a protected API response only when a deterministic spending policy authorizes it.

Payments are bound to exact requests and protected through merchant allowlists, spending limits, expiration checks, audit events, authorization revocation, and replay prevention.

The project includes a TypeScript monorepo, protected API, policy engine, agent runner, dashboard, Casper adapter, and an Odra smart contract for recording proof data on Casper Testnet.

**Demonstrates:** agentic commerce · HTTP 402 · policy engines · request-bound receipts · replay protection · programmable authorization · Casper Testnet · on-chain proof recording

**Stack:** TypeScript · Node.js · Next.js · Rust · Odra · Casper · Vitest

[Live demo](https://cspr-agentpay-guard.vercel.app/) · [Source code](https://github.com/alsaecas/cspr-agentpay-guard) · [DoraHacks submission](https://dorahacks.io/buidl/46706)

---

### 🏦 CupTreasury

**A self-custodial treasury for football teams, squads, and fan groups.**

CupTreasury replaces contribution reminders and expense approvals managed through WhatsApp with a structured treasury workflow.

Captain and Treasurer approvals are transformed into exact, one-time payment capabilities that can be evaluated through Tether WDK policies.

The project includes contribution tracking, match-day expense requests, role-based approvals, PaymentIntent authorization, WDK policy simulation, safe no-broadcast signing, proof artifacts, automated tests, and a judge-facing verification flow.

**Demonstrates:** programmable payments · self-custody · approval policies · capability-based authorization · Tether WDK · payment intents · security boundaries

**Stack:** Next.js · TypeScript · Tether WDK · React · Vitest · GitHub Actions

[Live demo](https://cuptreasury.vercel.app/) · [Source code](https://github.com/alsaecas/cuptreasury) · [DoraHacks submission](https://dorahacks.io/buidl/46738)

---

### 🔄 SwapGuard

**A security-aware Uniswap V2 integration with slippage protection and reproducible fork testing.**

SwapGuard demonstrates the complete ERC-20 swap lifecycle: router quotations, exact-input swaps, minimum-output protection, transaction deadlines, temporary router allowances, direct output delivery, and transaction receipt handling.

The project includes a focused Solidity integration contract, behavioural mocks, unit and fuzz tests, pinned Arbitrum fork tests against real deployed contracts, local Anvil tooling, CI, and a React interface built with wagmi and viem.

The public deployment is an interactive portfolio preview. Real swap execution is available through the reproducible local Arbitrum fork without using real funds.

**Demonstrates:** DeFi integration · Uniswap V2 · ERC-20 allowances · slippage protection · router trust boundaries · fork testing · wallet transaction UX

**Stack:** Solidity · Foundry · OpenZeppelin · React · TypeScript · wagmi · viem · Arbitrum · Anvil · Vercel

[Interactive demo](https://swapguard-zeta.vercel.app/) · [Source code](https://github.com/alsaecas/swapguard)

---

### ✈️ On-chain Flight Turnaround Checklist

**Winner of the Blockchain-based Turnaround Checklist challenge at Decode Travel Barcelona 2025.**

A smart-contract-backed aviation workflow created with Camino Network and Vueling.

Each aircraft turnaround is modelled through task ownership, role permissions, completion states, operational deadlines, SLA and KPI computation, certification, and ERC-721 reward badges.

The project translates a real multi-actor operational process into explicit, auditable smart-contract state transitions.

**Demonstrates:** operational workflow modelling · smart-contract state machines · deadlines · KPIs · certification · tokenized incentives

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

## Production backend and identity engineering

Alongside my public Web3 and product work, I build backend and identity systems using **Kotlin, Java, Spring Boot, PostgreSQL, Keycloak, REST APIs, OpenAPI, Docker, Gradle, and CI/CD**.

My professional work includes:

* Identity federation, SSO, authentication flows, and role synchronization
* Custom Keycloak authenticators, event listeners, storage providers, and client policies
* OAuth2 and OpenID Connect integrations
* REST and gRPC service design
* PostgreSQL database modelling and Flyway migrations
* External provider and blockchain integrations
* Authorization and account-lifecycle rules
* Background messaging and asynchronous processing
* Automated unit, integration, and controller testing
* Production debugging, dependency upgrades, migrations, and deployment workflows

---

## Technical focus

| Area                       | Technologies and concepts                                                                                              |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Backend systems**        | Kotlin, Java, Spring Boot, Node.js, TypeScript, REST, gRPC, PostgreSQL, MongoDB, OpenAPI                               |
| **Identity and security**  | Keycloak, SSO, OAuth2, OpenID Connect, identity federation, RBAC, policy enforcement                                   |
| **Smart contracts**        | Solidity, Foundry, Hardhat, OpenZeppelin, EVM, ERC-20, ERC-721, ERC-1155, EIP-712                                      |
| **Token distribution**     | Presales, phased pricing, soft caps, escrow, refunds, TGE unlocks, cliffs, linear vesting                              |
| **DeFi and payments**      | Uniswap V2, token allowances, slippage, Chainlink-compatible feeds, oracle normalization, Tether WDK, payment policies |
| **Smart-contract testing** | Unit tests, fuzz tests, stateful invariants, behavioural mocks, fork tests, reentrancy testing                         |
| **Blockchain ecosystems**  | Ethereum, Sepolia, Arbitrum, Camino Network, Casper, wallets, transaction receipts, IPFS                               |
| **Mobile products**        | React Native, Expo, Android, iOS, Expo Router, TanStack Query, Jotai, EAS Build, Maestro                               |
| **Frontend and Web3 UX**   | React, Next.js, TypeScript, wagmi, viem, RainbowKit, dashboards, marketplaces, wallet flows                            |
| **Infrastructure**         | Docker, Docker Compose, GitHub Actions, GitLab CI/CD, Gradle, Vercel, AWS services                                     |
| **Industrial systems**     | PLCs, SCADA, automation, controls, OT/IT integration, automotive production                                            |

---

## More Solidity and EVM work

<details>
<summary><strong>View additional smart-contract projects</strong></summary>

<br/>

### Fallas Passport

Location-based ERC-1155 passport using EIP-712 signed vouchers, QR/NFC checkpoints, replay protection, and privacy-aware presence verification.

[View repository](https://github.com/alsaecas/fallas-passport-1155)

### Fixed-Amount ERC-20 Staking

Fixed-token staking system with period-based ETH rewards, SafeERC20 handling, custom errors, administrative boundaries, and security-focused Foundry tests.

[View repository](https://github.com/alsaecas/erc20-staking-eth-rewards)

### SavingsBankPro

Time-locked ETH savings plans with early-withdrawal penalties, treasury routing, pause controls, reentrancy protection, and fuzz testing.

[View repository](https://github.com/alsaecas/savings-bank-pro-foundry)

### Chain Bounty Marketplace

ERC-20-funded bounty marketplace with escrow, submissions, deadlines, winner selection, cancellation rules, and payout execution.

[View repository](https://github.com/alsaecas/Chain-Bounty-Marketplace)

</details>

---

## How I approach engineering

* Start with the actors, rules, assets, constraints, and failure modes—not the framework.
* Keep contract, application, database, and API state transitions explicit and testable.
* Treat authentication, wallets, signatures, providers, mobile platforms, tokens, price feeds, and external protocols as reliability boundaries.
* Design administrative permissions around least privilege and clearly defined responsibilities.
* Preserve user claims, refunds, escrowed assets, and protocol liabilities during failure and recovery paths.
* Separate demonstrable functionality from assumptions, simulations, and future production work.
* Use blockchain where it provides verifiable state, traceability, programmable authorization, or meaningful automation.
* Test isolated behaviour with mocks and external integrations against reproducible environments.
* Combine example-based tests with fuzzing, invariants, fork tests, and end-to-end validation where appropriate.
* Validate critical product journeys across the platforms, networks, wallets, and device states where they run.
* Document architecture, mathematics, trust assumptions, limitations, deployment evidence, and production-hardening requirements.

---

## Currently exploring

* Secure token distribution, escrow, refund, and vesting architectures
* Autonomous-agent payments and HTTP 402 workflows
* Policy-controlled wallets and programmable payment authorization
* DeFi protocol integrations and secure token flows
* Chainlink-compatible oracle validation and decimal normalization
* Stateful invariant testing and reproducible mainnet-fork environments
* On-chain proof, audit, and verification systems
* Blockchain-backed operational workflows
* Reliable cross-platform applications connected to backend and identity systems

---

## Let’s connect

I am open to remote opportunities involving **senior backend engineering, smart contracts, DeFi integrations, token infrastructure, blockchain platforms, Web3 security, identity systems, programmable payments, production mobile products, and technically ambitious product development**.

[Portfolio](https://www.alsaecas.dev/) · [LinkedIn](https://www.linkedin.com/in/alejandrosaezc/) · [Contact](https://www.alsaecas.dev/contact)
