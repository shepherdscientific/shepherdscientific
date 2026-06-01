# Ifedayo Oladapo

**Systems Architect | Blockchain Infrastructure | Hardware Security | AI/ML Engineering**

Building production-grade systems from embedded automotive (Bosch Engineering) to DeFi infrastructure and post-quantum cryptographic hardware.
Specialized in compliant financial systems, fraud detection, multichain architecture, and secure hardware design.

Danish/Nigerian dual citizen 🇩🇰🇳🇬 | Based in Lagos | Available globally

---

## 🔨 Selected Open Source Work

### [🔁 Mr. Wiggum — Multi-tool Autonomous AI Agent Loop](https://github.com/shepherdscientific/mr-wiggum)

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Fork of Ralph](https://img.shields.io/badge/Fork%20of-snarktank%2Fralph-orange)](https://github.com/snarktank/ralph)
[![Status](https://img.shields.io/badge/Status-Active-success)](README.md)

A heavily extended fork of [Ralph](https://github.com/snarktank/ralph) — the autonomous AI agent loop that runs AI coding tools repeatedly until all PRD items are complete. Where Ralph supports Amp and Claude Code, Mr. Wiggum goes further.

**Stack:** Bash, JSON, Markdown  
**What this fork adds:**
- **Multi-tool support** — Amp, Claude Code, OpenCode, Gemini CLI, or Codex; each with its own optimised prompt file
- **Agent persona injection** — 27 specialist personas (backend architect, security engineer, reality checker, etc.) assigned per story or whole PRD
- **Aider code review gate** — reviews every diff before committing; critical issues must be fixed before the loop continues
- **Provider-agnostic review** — review step works against local LLM, Gemini, DeepSeek, or any OpenAI-compatible API
- **PATCH-not-REWRITE guards** — prompt files explicitly prevent silent regressions from full file rewrites
- **Live STDOUT streaming** — output streamed to terminal in real time via `/dev/tty`

[View on GitHub →](https://github.com/shepherdscientific/mr-wiggum)

---

### [🔐 TernaryCore PQC Reference Wallet](https://github.com/shepherdscientific/wallet-hardware)

[![License: CERN-OHL-S-2.0](https://img.shields.io/badge/License-CERN--OHL--S--2.0-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-ESP32--S3-red)](platformio.ini)
[![Status](https://img.shields.io/badge/Status-Lab%20Evaluation-yellow)](README.md)

Open-source client application layer, UI state machines, and hardware abstraction layers for the TernaryCore post-quantum cryptographic reference architecture. Built on the CoinCube dual-tactile menu framework, routes cryptographic operations through a compile-time selectable secure element HAL.

**Stack:** C++, Arduino/ESP32, PlatformIO  
**Hardware:** ESP32-S3 + SSD1306 128×64 OLED + 2-button UI + Microchip ATECC608B / TernaryCore FPGA SE  
**SE HAL Targets:** `USE_SE_STUB` (software) · `USE_ATECC608B` (legacy I2C) · `USE_TERNARYCORE_SE` (FPGA UART)  
**Features:** BIP39/32/44, PSBT signing, air-gapped operation, anti-phishing device pairing, firmware integrity attestation

> ⚠️ Academic/evaluation only — not certified for production key custody

[View on GitHub →](https://github.com/shepherdscientific/wallet-hardware)

---

### [🧮 pqc-secure-element — TernaryCore FPGA Secure Element](https://github.com/shepherdscientific/pqc-secure-element)

[![License: CERN-OHL-S-2.0](https://img.shields.io/badge/License-CERN--OHL--S--2.0-blue.svg)](LICENSE)
[![FPGA](https://img.shields.io/badge/FPGA-Tang%20Nano%209K-purple)](constr/tangnano.cst)
[![Status](https://img.shields.io/badge/Status-Phase%202-yellow)](README.md)

Gowin GW1NR-9C FPGA implementation of the TernaryCore secure element. A PicoRV32 RISC-V soft-core runs a bare-metal AT-command firmware over UART, providing ECDSA signing, secp256k1 key storage, TRNG, and SHA-256 — all implemented in RTL with a ternary polynomial multiplier for Phase 3 PQC acceleration.

**Stack:** Verilog, RISC-V (RV32IM), Gowin EDA, C (bare-metal)  
**Hardware:** Sipeed Tang Nano 9K (GW1NR-LV9QN88PC6/I5)  
**RTL Modules:** `picorv32`, `wb_uart`, `ternary_mac`, `ternary_poly_mul`, `barrett_reduce`  
**Protocol:** AT-command UART 115200 8N1 · `AT+INFO` · `AT+RAND` · `AT+SIGN:ECDSA` · `AT+PUBKEY`

[View on GitHub →](https://github.com/shepherdscientific/pqc-secure-element)

---

### [📡 Neural Spatial Upscaler](https://github.com/shepherdscientific/neural-spatial-upscaler)

[![License: CERN-OHL-S-2.0](https://img.shields.io/badge/License-CERN--OHL--S--2.0-blue.svg)](LICENSE)
[![FPGA](https://img.shields.io/badge/Target-Alveo%20U50-blue)](README.md)
[![Status](https://img.shields.io/badge/Status-Design%20Phase-orange)](README.md)

RTL implementation of a neural spatial upscaling module targeting the Xilinx Alveo U50 HBM2 FPGA. Designed to accelerate edge-ML inference for video/image upscaling workloads without a discrete GPU.

**Stack:** Verilog/SystemVerilog, HLS, Python  
**Hardware:** Xilinx Alveo U50 (HBM2, 100G QSFP28)  
**Approach:** Tiled systolic array with HBM2 line buffers, sub-pixel convolution, INT8 quantised weights

[View on GitHub →](https://github.com/shepherdscientific/neural-spatial-upscaler)

---

### [🚀 Optimized SSSP Implementation](https://github.com/shepherdscientific/optimized-sssp/)

[![Status](https://img.shields.io/badge/Status-Active-success)](README.md)

Research implementation of optimized Single-Source Shortest Path algorithms, progressing from classical Dijkstra toward structured paths achieving O(m log^{2/3} n) complexity.

**Stack:** Rust  
**Focus:** Algorithm optimization, graph theory, benchmarking

[View on GitHub →](https://github.com/shepherdscientific/optimized-sssp/)

---

### 📊 BadDocs — AI-Powered Documentation Tool
*Not yet open-sourced*

Intelligent documentation generation and management system. Built after experiencing too many projects with outdated or missing docs.

**Stack:** Python, LLM Integration, Markdown  
**Features:** Smart content generation, quality metrics, workflow integration

---

### 📡 SignalBeam — ESP32 Webhook Notification Display
*Hardware tested — software refinement*

Real-time webhook visualization system using LED matrix displays for DevOps monitoring and GitHub integration.

**Stack:** C++, ESP32, WebSockets, REST APIs  
**Hardware:** ESP32, MAX7219 LED matrix

---

## 🔬 Blockchain Research & Reference Implementations
*Educational implementations and architecture patterns*

### DeFi Trading Strategies
Reference implementations for cryptocurrency arbitrage detection and execution across DEXs. Includes MEV awareness and gas optimization strategies.

**Topics:** Cross-DEX arbitrage, flash loans, triangular arbitrage, slippage calculation

### DAO Governance Frameworks
Modular DAO architecture patterns with token-weighted, quadratic, and conviction voting mechanisms and treasury management strategies.

**Topics:** On-chain governance, proposal systems, timelock execution, multi-sig integration

### Token Distribution Systems
Airdrop mechanisms, vesting schedules, and merkle tree-based claim systems with sybil resistance patterns.

**Topics:** Merkle airdrops, linear/cliff vesting, snapshot strategies, fair launch patterns

### Consensus Mechanisms
Educational implementations of PoW, PoS, and hybrid consensus focused on understanding tradeoffs and attack vectors.

**Topics:** Mining difficulty adjustment, validator selection, slashing conditions, finality

### Fundraising Smart Contracts
ICO/IDO mechanisms, bonding curves, Dutch auctions, and token sale patterns with proper access control and emergency mechanisms.

**Topics:** Price discovery, contribution caps, refund mechanisms, vesting integration

*Reference implementations for educational purposes. Production use requires comprehensive auditing and customization.*

---

## 🏦 Blockchain & Financial Infrastructure Experience
*Architecture and consulting work — specific implementations under NDA*

- **Smart Contract Architecture:** Upgradeable proxy patterns (UUPS), role-based access control, regulatory compliance frameworks
- **AI Fraud Detection:** Predictive systems for high-transaction banking environments with real-time risk assessment
- **Banking Integration:** Core banking system architecture and payment processing infrastructure
- **Product Stabilization:** Took high-disruption products to zero critical incidents through systematic engineering

*Available to discuss architecture patterns and problem-solving approaches in detail*

---

## 💡 Technical Background

**Current Focus:**
- Post-quantum cryptographic hardware (FPGA secure elements, PicoRV32 RISC-V)
- DeFi infrastructure and stablecoin architecture
- AI/ML fraud detection systems
- Agentic AI workflows and automation (Mr. Wiggum, Ralph pattern)
- Web3 security and smart contract auditing

**Previous Work:**
- **Bosch Engineering:** Embedded diesel powertrain systems, production automotive solutions for major OEMs
- **GRIT Systems Engineering:** IoT energy metering, blockchain-based P2P electricity trading research
- **Digital Financial Services:** Investment product platforms and payment systems architecture

**Teaching & Mentorship:**
Alumni from teams I've built have gone on to secure pre-seed funding, publish in IEEE conferences, and receive patents for their innovations.

---

## 🛠️ Tech Stack

**Blockchain & Smart Contracts:**
```
Solidity, Hardhat, Foundry, Remix, Tendermint, Hyperledger
Web3.js, Ethers.js, OpenZeppelin
UUPS Proxies, Diamond Pattern, Access Control
```

**AI/ML & Data:**
```
Python, TensorFlow, PyTorch, PEFT
Fraud Detection Models, Credit Scoring
Predictive Analytics, Time Series Analysis
```

**Systems & Backend:**
```
Go, Rust, C/C++, Python
Microservices, Event-Driven Architecture
Real-time Processing, Low-Latency Systems
```

**Fintech & Banking:**
```
Core Banking Systems, Banking as a Service
Payment Processing, KYC/AML Integration
NIBSS, Central Banking Aggregators
```

**Hardware & Embedded:**
```
ESP32, STM32, Arduino, RISC-V (PicoRV32)
Gowin / Xilinx FPGA (Verilog, Gowin EDA)
Real-time Operating Systems (RTOS)
Automotive Powertrains, IoT Devices
```

---

## 📜 Certifications

- **Certified Blockchain Auditor** — In progress
- **B.Sc.Eng (Hons)** — Electrical and Computer Engineering, University of Southern Denmark (2002)

---

## 🌍 Languages

- **English** (Fluent)
- **German** (Fluent)
- **Danish** (Fluent)
- **Yoruba** (Native)
- **French** (Conversational)

---

## 💼 Available For

- **Fractional CTO engagements** for fintech and blockchain startups
- **Blockchain architecture consulting** for DeFi protocols and stablecoin projects
- **Technical due diligence** for investors evaluating blockchain projects
- **Smart contract security audits**
- **Fraud detection system design** for financial services
- **Secure hardware architecture** for embedded and IoT products

**Not available for:**
- Full-time roles requiring relocation outside Nigeria
- Projects without clear scope and timelines
- Equity-only compensation arrangements

---

## 📫 Get In Touch

**Email:** ifedayo.oladapo@gmail.com  
**LinkedIn:** [linkedin.com/in/ifedayo-oladapo](https://linkedin.com/in/ifedayo-oladapo)  
**Location:** Lagos, Nigeria (🇩🇰 EU work authorization available)

**Response time:** Usually within 24 hours for project inquiries

---

## 📊 GitHub Stats

![Profile Views](https://komarev.com/ghpvc/?username=shepherdscientific&color=blueviolet)

---

<sub>💡 **Open to collaboration** on DeFi infrastructure, fraud detection systems, blockchain education projects in Africa, and open hardware security research.</sub>

<sub>⚡ **Fun fact:** I built production automotive systems before building production DeFi systems — turns out the attention to safety and reliability transfers well. Now I'm doing both simultaneously in hardware wallet silicon.</sub>
