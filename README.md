# Genmount WorldModel-OS

> **L1 platform skeleton — the operating system layer for auditable agentic reasoning.**

[![Paper DOI](https://img.shields.io/badge/Paper%20DOI-10.5281%2Fzenodo.20053545-1682d4)](https://doi.org/10.5281/zenodo.20053545)
[![Status](https://img.shields.io/badge/status-pending%20%C2%A711%20gates-orange)](https://github.com/doorm-ai/Genmount-WorldModel-OS-Governance#three-release-gates-per-11-of-the-paper)
[![Last Commit](https://img.shields.io/github/last-commit/doorm-ai/Genmount-WorldModel-OS)](https://github.com/doorm-ai/Genmount-WorldModel-OS/commits/main)
[![Stars](https://img.shields.io/github/stars/doorm-ai/Genmount-WorldModel-OS?style=social)](https://github.com/doorm-ai/Genmount-WorldModel-OS/stargazers)
[![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0--or--later-blue.svg)](https://www.gnu.org/licenses/agpl-3.0.html)

**Coming soon. Not released yet — by design.**

This is the L1 platform skeleton of the **DOORM Genmount WorldModel-OS** architecture: a hybrid local/cloud operating system for agentic world models that puts **auditable rollback, state-space discipline, and disclosure boundaries** ahead of scale.

---

## 🎯 What WorldModel-OS solves

Modern agentic LLMs ship a fundamental contradiction: they are tasked with high-stakes domains (medical, legal, financial) but lack the structural primitives to be audited. Hallucination is treated as a tax, not a fault. Rollback is a nice-to-have, not a contract.

WorldModel-OS treats audit as a **first-class architectural concern**, not retrofit:

- **Discrete anchor state-space** — every inference produces a coordinate in an 8 / 64 / 384 anchor space, not just free-form text
- **Four-level rollback contract** embedded in every inference trace
- **Redactor + append-only audit trail** built into the gateway, not bolted on
- **L1 / L2 / L3 disclosure boundary** — what's open, what's closed, and why

---

## 🚀 What's coming (in this repo)

When released, this repository will contain:

| Module | Purpose |
|---|---|
| `gateway/` | Request entry, authentication, rate limiting, redactor |
| `state_space/` | 8 / 64 / 384 anchor encoding + decoding |
| `audit/` | Append-only trace store + four-level rollback hooks |
| `redactor/` | PII and clinical-data egress filter |
| `runtime/` | L2 adapter handshake + `adapter_version` pinning |

**Base-model agnostic** — orchestrates any compliant L2 adapter.

---

## 🚦 Release status

| Gate (§11 of paper) | Status |
|---|---|
| Reproducibility (single-GPU 24h reference run) | ⏳ Pending |
| Benchmark (TCM syndrome differentiation + rehabilitation) | ⏳ Pending |
| Real-adoption (MOU or paid deployment) | ⏳ Pending |

All three must pass before this repository goes public. **No code release for demo's sake.**

> See [§11 of the companion paper](https://github.com/doorm-ai/Genmount-WorldModel-OS-Governance#three-release-gates-per-11-of-the-paper) for full gate definitions and falsification criteria.

---

## 🔭 Architecture context

| Tier | Status | Scope | This repo? |
|---|---|---|---|
| **L3** Production artifacts | 🔒 Closed | Production weights, clinical adapters, partner data, device auth keys | No |
| **L2** Finetune Workbench | ⏳ Pending | Training pipeline + three hard quality gates | Sibling repo |
| **L1** Platform skeleton | ⏳ Pending | Gateway · State space · Audit · Redactor · Runtime | **← You are here** |

L2 produces adapters. L1 consumes them. They communicate via a stable `adapter_version` handshake — neither is locked to the other's release schedule.

---

## 📡 Stay updated

- **⭐ Star** this repo to track release
- **👁 Watch → Custom → Releases** for the first public drop notification
- **💬 [Discussions](https://github.com/doorm-ai/Genmount-WorldModel-OS/discussions)** for early design feedback
- **📬 [Issues](https://github.com/doorm-ai/Genmount-WorldModel-OS/issues)** for post-release bug reports

---

## 📚 Companion artifacts

- 📄 **[Paper + governance docs](https://github.com/doorm-ai/Genmount-WorldModel-OS-Governance)** — DOI [10.5281/zenodo.20053545](https://doi.org/10.5281/zenodo.20053545)
- 🛠 **[Finetune-Workbench](https://github.com/doorm-ai/Genmount-Finetune-Workbench)** — L2 training workbench (sibling repo)

---

## 💼 Commercial / non-AGPL licensing

For commercial deployment outside AGPL-3.0-or-later terms, partner integrations, or clinical L3 access:

📧 **service@doorm.ai**

DOORM AI PTE. LTD. (UEN 202441729W) · Singapore
