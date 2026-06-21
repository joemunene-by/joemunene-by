<div align="center">

# Joe Munene

### Founder, [Complex Developers](https://github.com/complexdevelopers)

I build security-focused AI systems from the model up: language models trained from scratch,<br>
the agent runtimes that make them safe to deploy, and production security tooling around them.

Currently building **[GhostLM](https://github.com/joemunene-by/GhostLM)**, an 81M-parameter cybersecurity language model trained from scratch in PyTorch, and **[ghostloop](https://github.com/joemunene-by/ghostloop)**, a fail-closed safety runtime for embodied agents, published on PyPI (`pip install ghostloop`) with a [Next.js control plane](https://github.com/joemunene-by/ghostloop-ui), a [Tauri desktop app](https://github.com/joemunene-by/ghostloop-desktop), and a [live HuggingFace demo](https://huggingface.co/spaces/Ghostgim/ghostloop-demo).

<br>

[![ghostloop on PyPI](https://img.shields.io/pypi/v/ghostloop?label=ghostloop%20on%20PyPI&color=14B8A6&style=flat-square)](https://pypi.org/project/ghostloop/)
[![GhostLM on HuggingFace](https://img.shields.io/badge/GhostLM-HuggingFace-FFD21E?style=flat-square)](https://huggingface.co/Ghostgim/GhostLM-v0.9-experimental)
[![Portfolio](https://img.shields.io/badge/Portfolio-6C9CFF?style=flat-square)](https://my-portfolio-peach-eta-42.vercel.app)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square)](mailto:joemunene984@gmail.com)

</div>

<br>

## `> whoami`

I'm Joe Munene, founder of **[Complex Developers](https://github.com/complexdevelopers)**, building from Nairobi, Kenya. The throughline across what I ship is systems that stay auditable under adversarial conditions, from model internals to agent runtime. The [studio's platform and CRM](https://github.com/complexdevelopers/Complex-Developers-Web) runs on Next.js 15, Prisma, and Postgres.

I study Computer Science at **Moi University**. In parallel I have trained a language model from scratch, published a safety runtime to PyPI, and merged work upstream into AutoGPT. Roughly 785,000 lines of first-party code across 50+ repositories. The shortest way to prove what you can engineer is to show working code, so that is what this profile is.

<br>

## `> git log --grep="upstream"`

<table>
<tr>
<td width="50%" valign="top">

### [AutoGPT #12805](https://github.com/Significant-Gravitas/AutoGPT/pull/12805)
**Merged** into Significant-Gravitas/AutoGPT, one of the most-starred AI projects on GitHub. Fixed agent name preservation in `AgentExecutor` node titles after page reload in the visual builder frontend. Small surface, high visibility: it surfaces every time a user reopens a saved graph.

</td>
<td width="50%" valign="top">

### [pytorch/ignite #3741](https://github.com/pytorch/ignite/pull/3741)
**Open, under review.** Replaces the naive `E[X²] − E[X]²` variance formula in `PearsonCorrelation` with **Welford's online algorithm** plus a parallel distributed merge. Fixes catastrophic cancellation in float32 (the metric was returning 0.89 instead of 0.99 for `mean=1e6` data). Numerically stable across single-process and DDP.

</td>
</tr>
</table>

<br>

## `> ps aux | grep active`

<table>
<tr>
<td width="50%" valign="top">

### Currently shipping: GhostLM
An open source cybersecurity language model built from scratch in PyTorch. 81M parameter decoder-only transformer (RoPE, SwiGLU, RMSNorm) trained on a 422M token multi-domain corpus across 27 sources: cybersec writeups, NVD CVEs, MITRE / CWE / OWASP, NIST SP 800, FineWeb-Edu, open-web-math, and a 105 repo open source code pull spanning 15 languages.

Ships GhostAgent (a tool-using runtime), a multi-vendor HTTP server speaking OpenAI / Anthropic / Gemini / Ollama wire formats, an MCP server, and GhostBench (a packaged eval suite with Wilson 95% CIs and McNemar paired comparisons across 14 differentiation bets). 312 tests green. [View the repo](https://github.com/joemunene-by/GhostLM).

### What I ship

**AI agent safety stack**: secure-mcp, ghostguard (4-tier policy proxy with audit dashboard), CyberBench

**Defensive security toolkit**: ghostaudit (23 CIS Kubernetes checks), ghostforensics (memory forensics with YARA + Volatility + STIX 2.1 export), ghostsiem (Sigma-rule SIEM), securecommit (pre-commit secret scanner)

**Offensive tooling**: concurrent TCP port scanner, packet-level traffic analyzer, vulnerability scanner, hash-cracking framework, MAC rotator, metadata scrubber

**The ghost security suite**: eleven production CLI tools spanning recon, web and mobile scanning, ML intrusion detection, malware triage, supply chain, cloud posture, and key management (listed below)

**Full-stack platforms**: Complex Developers CRM (Next.js 15 + Prisma + Postgres), ChartSentinel (trading SaaS with Stripe + PostHog + Sentry), High-End CRM, ai-coding-assistant

</td>
<td width="50%" valign="top">

### Latest drops

**[ghostloop v1.0.3](https://github.com/joemunene-by/ghostloop)** — the agent loop, embodied. `pip install ghostloop` (v1.0.3 on PyPI), [live HuggingFace demo](https://huggingface.co/spaces/Ghostgim/ghostloop-demo), full CI/CD with PyPI Trusted Publishing. Six simulation backends (MuJoCo / PyBullet / Gymnasium / ROS 2), 12 fail-closed policy gates, LLM + VLA policy adapters, and a bench harness with Wilson CI, McNemar, adversarial fuzzing (CMA-ES), STL temporal properties, counterfactual replay, and causal failure attribution. Production fleet dashboard with auth, rate limiting, alarms, and Prometheus. **359 tests green.**

**[ghostloop-ui](https://github.com/joemunene-by/ghostloop-ui)** — Next.js 15 + React 19 + Tailwind 4 control plane, live at [ghostloop-ui.vercel.app](https://ghostloop-ui.vercel.app). Fleet view, alarm tray, episode timeline, per-counter Prometheus metrics, and a profile-aware gamepad mapper (drone / mobile base / quadruped / arm / humanoid) built for non-coders. Demo-mode fallback keeps the deploy interactive with no backend configured.

**[ghostloop-desktop v0.2](https://github.com/joemunene-by/ghostloop-desktop)** — Tauri 2 + Rust shell wrapping ghostloop-ui as a single-file native app for macOS / Windows / Linux. Voice control, gamepad rumble on safety events (geofence block, force-cap trip, e-stop), native OS notifications, 120 Hz gamepad polling via `gilrs`, system-tray integration, and a global e-stop hotkey. Per-PR CI matrix green across all three platforms.

**[secure-mcp](https://github.com/joemunene-by/secure-mcp)** — MCP server exposing security tools to AI agents with policy gates, subprocess sandboxing, and audit trails. Fail-closed by default.

**[CyberBench](https://github.com/joemunene-by/cyberbench)** — Open, reproducible benchmark for evaluating LLMs on cybersecurity reasoning. YAML tasks, pluggable backends, ranked leaderboard.

**[linkdrop v0.7.1](https://github.com/joemunene-by/linkdrop)** — Cross-platform Tauri + Rust desktop app bridging iPhone to Linux for photos, files, notifications, screen mirroring. Daemon-backed pymobiledevice3 bridge, CI-built .deb / .AppImage.

</td>
</tr>
</table>

<br>

## `> ls /opt/ghost-suite`

Eleven production CLI security tools, shipped as one coherent suite. Every one is installable, test covered, and green on GitHub Actions CI across Python 3.11 and 3.12. 489 passing tests in total, console plus JSON plus SARIF output for CI gating, and authorized-use framing throughout.

<table>
<tr><th align="left">Tool</th><th align="left">Domain</th><th align="left">What it does</th></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostrecon">ghostrecon</a></td><td>Offensive, OSINT</td><td>Passive recon framework: cert transparency, DNS, Wayback, entity graph, HTML and JSON reports</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostmap">ghostmap</a></td><td>Offensive, AppSec</td><td>Web vulnerability scanner: auth-aware crawler plus XSS and SQLi injection engine, SARIF output</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostpwn">ghostpwn</a></td><td>Offensive, Orchestration</td><td>Pentest workflow engine: YAML stages, dependency DAG, parallel execution, consolidated report</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostscope">ghostscope</a></td><td>Defensive, ML</td><td>AI intrusion detection: IsolationForest and PyTorch autoencoder on flow features, explainable alerts</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostbox">ghostbox</a></td><td>Defensive, Malware</td><td>Static malware sandbox: PE and ELF parsing, entropy and packer heuristics, IOC extraction, YARA, threat score</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostdlp">ghostdlp</a></td><td>Defensive, Data</td><td>Data-leak prevention and PII classifier: 16 validated detectors (Luhn, IBAN, ABA, entropy), masking and redaction</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostsbom">ghostsbom</a></td><td>Supply chain</td><td>Supply-chain analyzer: CycloneDX SBOM, OSV.dev CVE scan, typosquat and maintainer-risk signals</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostchain">ghostchain</a></td><td>Web3, AppSec</td><td>Solidity static auditor: 10 SWC-mapped detectors, console, JSON, and SARIF for code scanning</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostmobile">ghostmobile</a></td><td>Mobile, AppSec</td><td>APK and IPA static analyzer: dependency-free binary AndroidManifest decoder, 14 platform checks</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostcloud">ghostcloud</a></td><td>Cloud, CSPM</td><td>Multi-cloud posture scanner: 17 AWS, GCP, and Azure misconfiguration checks with remediation</td></tr>
<tr><td><a href="https://github.com/joemunene-by/ghostvault">ghostvault</a></td><td>Cryptography, KMS</td><td>Key management system: DEK and KEK envelope encryption (AES-256-GCM, scrypt), rotation, AAD binding, audit log</td></tr>
</table>

<br>

## `> man joe`

Technical writing lives in **[joemunene-by/writing](https://github.com/joemunene-by/writing)**.

- **[AI Model Supply Chain Security](https://github.com/joemunene-by/writing/blob/main/ai-model-supply-chain-security.md)** — architectural guidance on serialization risks in model artifacts (pickle / `.pt` code execution, safetensors and ONNX alternatives), provenance verification, artifact scanning, and Model Bills of Materials. Originally proposed to the OWASP Cheat Sheet Series ([PR #2111](https://github.com/OWASP/CheatSheetSeries/pull/2111)) and revised through maintainer review.

<br>

## `> cat /etc/skills`

**Systems and AI.** Python and PyTorch, with transformers written from scratch (no framework abstractions): training, tokenization, and evaluation with proper statistics. Rust, TypeScript, and C. MCP servers and multi-vendor LLM serving.

**Security.** Offensive (recon, web and mobile scanning, exploitation tooling) and defensive (intrusion detection, malware triage, SIEM, memory forensics, cloud posture, key management). YARA, Sigma, STIX, CIS benchmarks.

**Product.** Full-stack web (Next.js, React, Tailwind, Postgres, Prisma), cross-platform desktop (Tauri, Rust), and mobile (React Native, shipped to the Google Play Store).

**Infrastructure.** Docker, Kubernetes, Terraform, GitHub Actions, Prometheus, and CI/CD with PyPI trusted publishing.

<br>

## `> tail -f`

Next: ghost-base, the ~360M-parameter successor to GhostLM, training on rented GPU. I take on select work in backend systems, security reviews, and API hardening.

**Joe Munene** · Founder, Complex Developers · Nairobi, Kenya · [joemunene984@gmail.com](mailto:joemunene984@gmail.com)
