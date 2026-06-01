# Ifedayo Oladapo

**Systems Architect | Blockchain Infrastructure | Hardware Security | AI/ML Engineering**

Building production-grade systems from embedded automotive (Bosch Engineering) to DeFi infrastructure and post-quantum cryptographic hardware.
Specialized in compliant financial systems, fraud detection, multichain architecture, and secure hardware design.

Danish/Nigerian dual citizen 🇩🇰🇳🇬 | Based in Lagos | Available globally

---

## 🗺️ Project Matrix

| Repo | Stack | Status | Tested | License |
|------|-------|--------|--------|---------|
| [mr-wiggum](https://github.com/shepherdscientific/mr-wiggum) | Bash, JSON | Active | ✅ Yes | MIT |
| [bio-agi](https://github.com/shepherdscientific/bio-agi) | Python, LIF sim | Active | ✅ Yes | MIT |
| [wallet-hardware](https://github.com/shepherdscientific/wallet-hardware) | C++, ESP32 | Lab eval | ✅ Yes | CERN-OHL-S v2 |
| [pqc-secure-element](https://github.com/shepherdscientific/pqc-secure-element) | Verilog, RISC-V | Phase 2 | ⚠️ Partial | CERN-OHL-S v2 |
| [auto-vision-cut](https://github.com/shepherdscientific/auto-vision-cut) | Python, MLX | Active | ⚠️ Partial | MIT |
| [neural-spatial-upscaler](https://github.com/shepherdscientific/neural-spatial-upscaler) | Verilog, HLS | Design phase | ❌ No | CERN-OHL-S v2 |
| [llama-server-tuning](https://github.com/shepherdscientific/llama-server-tuning) | Bash, Python | Active | ✅ Yes | GPL-3.0 |
| [esp32-wireless-printserver](https://github.com/shepherdscientific/esp32-wireless-printserver) | C, ESP-IDF | Active | ⚠️ Partial | MIT |
| [repo-matrix-appscript](https://github.com/shepherdscientific/repo-matrix-appscript) | Node.js, Apps Script | Active | ⚠️ Partial | MIT |
| [optimized-sssp](https://github.com/shepherdscientific/optimized-sssp/) | Rust | Active | ⚠️ Partial | GPL-3.0 |
| BadDocs | Python, LLM | In development | ❌ No | Private |

---

## 🔨 Selected Open Source Work

### [🧠 bio-agi — Biology-Grounded AGI Scaffold](https://github.com/shepherdscientific/bio-agi)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success)](README.md)
[![Stack](https://img.shields.io/badge/Stack-Python%20%7C%20LIF%20Sim-blue)](README.md)

The fruit fly's actual connectome does the routing. Any LLM — local or remote — does the inference. No cloud required, no GPU required.

FlyWire mapped the complete wiring of an adult *Drosophila* brain — 138,000 neurons, 5 million synapses. bio-agi runs a real-time leaky integrate-and-fire simulation of that connectome, uses spike rates from known functional populations (mushroom body, central complex, fan-shaped body, lateral horn…) to decide *which* cognitive modules activate on each tick, and dispatches the activated modules to whichever LLM backend you configure.

**Stack:** Python, LIF simulation, SQLite  
**Inference backends:** BitNet (CPU-native) · Ollama / any OpenAI-compat server · Anthropic SDK · dry-run mock  
**Cognitive modules:** memory · world model · goal · reward · emotion · executive · critic gate  
**Built with:** [Mr. Wiggum](https://github.com/shepherdscientific/mr-wiggum) autonomous loop — 12 stories, 12 commits, self-built  
**Use cases:** on-premise email triage, personal knowledge base, interpretable security monitoring, neuropharmacology simulation

> The fly brain decides what thinks. You decide with what.

[View on GitHub →](https://github.com/shepherdscientific/bio-agi)

---

### [🔁 Mr. Wiggum — Multi-tool Autonomous AI Agent Loop](https://github.com/shepherdscientific/mr-wiggum)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Fork of Ralph](https://img.shields.io/badge/Fork%20of-snarktank%2Fralph-orange)](https://github.com/snarktank/ralph)
[![Status](https://img.shields.io/badge/Status-Active-success)](README.md)

A heavily extended fork of [Ralph](https://github.com/snarktank/ralph) — the autonomous AI agent loop that runs AI coding tools repeatedly until all PRD items are complete.

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

### [🎬 AutoVisionCut — Local Vision-to-Edit Pipeline](https://github.com/shepherdscientific/auto-vision-cut)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-yellow)](README.md)
[![Platform](https://img.shields.io/badge/Platform-Apple%20Silicon-lightgrey)](README.md)

Transforms hours of raw OBS hardware prototyping footage into clean, narrative-driven videos — entirely locally. Treats video assembly as a code execution problem driven by local multimodal intelligence.

**Stack:** Python, FFmpeg, MLX/mlx-vlm, MoviePy  
**Pipeline:** FFmpeg frame extraction → local VLM scene analysis → Qwen3 script + cut-list generation → MoviePy render  
**Hardware:** Optimised for Apple Silicon M4 Pro unified memory (64GB)  
**Output artifacts:** `event_log.json` · `narration_script.md` · `cut_list.json` · `output_master.mp4`  
**Why local:** hardware IP stays private; no cloud bandwidth overhead for large raw recordings

[View on GitHub →](https://github.com/shepherdscientific/auto-vision-cut)

---

### [🔐 TernaryCore PQC Reference Wallet](https://github.com/shepherdscientific/wallet-hardware)

[![License: CERN-OHL-S-2.0](https://img.shields.io/badge/License-CERN--OHL--S--2.0-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-ESP32--S3-red)](platformio.ini)
[![Status](https://img.shields.io/badge/Status-Lab%20Evaluation-yellow)](README.md)

Open-source client application layer, UI state machines, and hardware abstraction layers for the TernaryCore post-quantum cryptographic reference architecture. Routes cryptographic operations through a compile-time selectable secure element HAL.

**Stack:** C++, Arduino/ESP32, PlatformIO  
**Hardware:** ESP32-S3 + SSD1306 128×64 OLED + 2-button UI + ATECC608B / TernaryCore FPGA SE  
**SE HAL Targets:** `USE_SE_STUB` · `USE_ATECC608B` · `USE_TERNARYCORE_SE` (FPGA UART)  
**Features:** BIP39/32/44, PSBT signing, air-gapped operation, anti-phishing device pairing, firmware integrity attestation

> ⚠️ Academic/evaluation only — not certified for production key custody

[View on GitHub →](https://github.com/shepherdscientific/wallet-hardware)

---

### [🧮 pqc-secure-element — TernaryCore FPGA Secure Element](https://github.com/shepherdscientific/pqc-secure-element)

[![License: CERN-OHL-S-2.0](https://img.shields.io/badge/License-CERN--OHL--S--2.0-blue.svg)](LICENSE)
[![FPGA](https://img.shields.io/badge/FPGA-Tang%20Nano%209K-purple)](constr/tangnano.cst)
[![Status](https://img.shields.io/badge/Status-Phase%202-yellow)](README.md)

Gowin GW1NR-9C FPGA implementation of the TernaryCore secure element. A PicoRV32 RISC-V soft-core runs bare-metal AT-command firmware over UART, providing ECDSA signing, secp256k1 key storage, TRNG, and SHA-256 — with a ternary polynomial multiplier for Phase 3 PQC acceleration.

**Stack:** Verilog, RISC-V (RV32IM), Gowin EDA, C (bare-metal)  
**Hardware:** Sipeed Tang Nano 9K (GW1NR-LV9QN88PC6/I5)  
**RTL Modules:** `picorv32` · `wb_uart` · `ternary_mac` · `ternary_poly_mul` · `barrett_reduce`  
**Protocol:** AT-command UART 115200 8N1 — `AT+INFO` · `AT+RAND` · `AT+SIGN:ECDSA` · `AT+PUBKEY`

[View on GitHub →](https://github.com/shepherdscientific/pqc-secure-element)

---

### [⚡ llama-server-tuning — KV Cache Benchmarking for Local Inference](https://github.com/shepherdscientific/llama-server-tuning)

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success)](README.md)

Benchmarking and tuning helpers for `llama-server` on local inference machines. Grew out of a practical question: do alternative KV cache strategies actually improve throughput, or just reduce memory?

**Stack:** Bash, Python  
**Scripts:** single/dual-endpoint benchmark · stepped one-at-a-time runner · ctx/batch/ubatch sweep · side-by-side comparison report  
**Published results:** Apple Silicon M4 Pro — f16 vs turbo3 KV across ctx 32K–245K, with throughput and RSS data  
**Key finding:** `f16` KV remained faster at moderate context; turbo3 wins only when memory pressure becomes the bottleneck at large context windows

[View on GitHub →](https://github.com/shepherdscientific/llama-server-tuning)

---

### [🖨️ esp32-wireless-printserver — WiFi→Ethernet Print Bridge](https://github.com/shepherdscientific/esp32-wireless-printserver)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-yellow)](README.md)
[![Stack](https://img.shields.io/badge/Stack-C%20%7C%20ESP--IDF-lightgrey)](README.md)

Firmware bridge between a modern WiFi network and a legacy wired printer, using ESP32 + W5500 Ethernet. Proxies raw TCP (port 9100), mDNS/Bonjour discovery, and IPP/AirPrint over a single low-cost microcontroller.

**Stack:** C, ESP-IDF, FreeRTOS, LwIP  
**Hardware:** ESP32 + W5500 (VSPI)  
**Protocols:** Raw TCP 9100 · mDNS · IPP/AirPrint · Captive portal config  
**Features:** NVS config persistence, HTTP config web form, WiFi auto-reconnect with exponential backoff

[View on GitHub →](https://github.com/shepherdscientific/esp32-wireless-printserver)

---

### [📊 repo-matrix-appscript — Repo Health Dashboard](https://github.com/shepherdscientific/repo-matrix-appscript)

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-yellow)](README.md)
[![Stack](https://img.shields.io/badge/Stack-Node.js%20%7C%20Apps%20Script-blue)](README.md)

Google Sheets + Apps Script dashboard that tracks repo health across GitHub (and other git hosts), with CI webhook integration and LLM-generated health summaries.

**Stack:** Node.js, Google Apps Script, clasp  
**Architecture:** Node.js core engine (data fetching, analysis, multi-git-host support) + thin Apps Script display layer (Sheets UI)  
**Features:** CI coverage webhooks · LLM health summaries · multi-provider support (GitHub, Forgejo, Gitea) · local Jest testing · Mac Mini persistent service mode  
**Output targets:** Google Sheets · JSON · web dashboard

[View on GitHub →](https://github.com/shepherdscientific/repo-matrix-appscript)

---

### [🚀 Optimized SSSP Implementation](https://github.com/shepherdscientific/optimized-sssp/)

[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-yellow)](README.md)

Research implementation of optimized Single-Source Shortest Path algorithms, progressing from classical Dijkstra toward structured paths achieving O(m log^{2/3} n) complexity.

**Stack:** Rust  
**Focus:** Algorithm optimization, graph theory, benchmarking

[View on GitHub →](https://github.com/shepherdscientific/optimized-sssp/)

---

### [📡 Neural Spatial Upscaler](https://github.com/shepherdscientific/neural-spatial-upscaler)

[![License: CERN-OHL-S-2.0](https://img.shields.io/badge/License-CERN--OHL--S--2.0-blue.svg)](LICENSE)
[![FPGA](https://img.shields.io/badge/Target-Alveo%20U50-blue)](README.md)
[![Status](https://img.shields.io/badge/Status-Design%20Phase-orange)](README.md)

RTL implementation of a neural spatial upscaling module targeting the Xilinx Alveo U50 HBM2 FPGA. Accelerates edge-ML inference for video/image upscaling workloads without a discrete GPU.

**Stack:** Verilog/SystemVerilog, HLS, Python  
**Hardware:** Xilinx Alveo U50 (HBM2, 100G QSFP28)  
**Approach:** Tiled systolic array with HBM2 line buffers, sub-pixel convolution, INT8 quantised weights

[View on GitHub →](https://github.com/shepherdscientific/neural-spatial-upscaler)

---

### 📊 BadDocs — AI-Powered Documentation Tool
*In development — not yet open-sourced*

Intelligent documentation generation and management system. Built after experiencing too many projects with outdated or missing docs.

**Stack:** Python, LLM Integration, Markdown  
**Features:** Smart content generation, quality metrics, workflow integration

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
- Biology-grounded AI architecture (FlyWire connectome, cognitive scaffolding)
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
LIF Neural Simulation, Connectome Routing
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

<sub>💡 **Open to collaboration** on DeFi infrastructure, fraud detection systems, blockchain education projects in Africa, open hardware security research, and biology-grounded AI.</sub>

<sub>⚡ **Fun fact:** I built production automotive systems before building production DeFi systems — turns out the attention to safety and reliability transfers well. Now I'm doing both simultaneously in hardware wallet silicon.</sub>
