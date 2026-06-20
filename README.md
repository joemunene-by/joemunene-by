<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0C0E14,50:6C9CFF,100:C4A1FF&height=200&section=header&text=Joe%20Munene&fontSize=50&fontColor=ffffff&fontAlignY=35&desc=Software%20Engineer%20%E2%80%A2%20Cybersecurity%20Researcher%20%E2%80%A2%20Founder%2C%20Complex%20Developers&descSize=15&descAlignY=55&descColor=8A8FA8&animation=fadeIn" width="100%" />

I build security tools, full-stack platforms, and AI systems from first principles.<br>
Not wrappers. Not tutorials. Production code that solves real problems.

Currently shipping **[GhostLM](https://github.com/joemunene-by/GhostLM)** — an 81M-parameter cybersecurity language model trained from scratch — and the **[ghostloop](https://github.com/joemunene-by/ghostloop)** family: an embodied-AI agent runtime with a fail-closed safety pipeline (`pip install ghostloop`), its [Next.js control plane](https://github.com/joemunene-by/ghostloop-ui), and a [Tauri desktop app](https://github.com/joemunene-by/ghostloop-desktop). Everything in one place at the [live HuggingFace demo](https://huggingface.co/spaces/Ghostgim/ghostloop-demo).

<br>

[![Portfolio](https://img.shields.io/badge/Portfolio-6C9CFF?style=for-the-badge&logo=vercel&logoColor=white)](https://my-portfolio-peach-eta-42.vercel.app)
[![Complex Developers](https://img.shields.io/badge/Studio-Complex_Developers-C4A1FF?style=for-the-badge&logo=react&logoColor=white)](https://github.com/complexdevelopers)
[![Email](https://img.shields.io/badge/Say_Hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:joemunene984@gmail.com)
[![GitHub](https://img.shields.io/badge/Follow-0C0E14?style=for-the-badge&logo=github&logoColor=white)](https://github.com/joemunene-by)

[![ghostloop on PyPI](https://img.shields.io/pypi/v/ghostloop?label=ghostloop&color=14B8A6)](https://pypi.org/project/ghostloop/)
[![Live demo](https://img.shields.io/badge/🤗%20live%20demo-Ghostgim%2Fghostloop--demo-FFD21E)](https://huggingface.co/spaces/Ghostgim/ghostloop-demo)
[![GhostLM on HuggingFace](https://img.shields.io/badge/🤗%20GhostLM-Ghostgim%2FGhostLM--v0.9-FFD21E)](https://huggingface.co/Ghostgim/GhostLM-v0.9-experimental)

</div>

<br>

## `> whoami`

I'm a Computer Science student at **Moi University** (Nairobi, Kenya) and the founder of **[Complex Developers](https://github.com/complexdevelopers)**, a studio that ships web platforms, custom tooling, and AI adjacent products. The [company site + CRM](https://github.com/complexdevelopers/Complex-Developers-Web) runs on Next.js 15, Prisma, and Postgres.

My work sits at the intersection of offensive security, full-stack engineering, applied AI, and systems programming. 50+ open source projects, 1,000+ commits, 4,154,000+ lines of code, and counting. The shortest way to prove what you can engineer is to show working code, so that's what this profile is.

<br>

## `> git log --grep="upstream"`

<table>
<tr>
<td width="50%" valign="top">

### [AutoGPT #12805](https://github.com/Significant-Gravitas/AutoGPT/pull/12805)
**Merged.** Fixed agent name preservation in `AgentExecutor` node titles after page reload in the visual builder frontend. Small fix, surfaces in the user flow every time you reopen a saved graph, so the regression was high-visibility once introduced.

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

Ships GhostAgent (a tool-using runtime), a multi-vendor HTTP server speaking OpenAI / Anthropic / Gemini / Ollama wire formats, an MCP server, and GhostBench (a packaged eval suite with Wilson 95% CIs and McNemar paired comparisons across 14 differentiation bets). 312 tests green.

[![GhostLM](https://img.shields.io/badge/View_Repo-GhostLM_v0.9.33-6C9CFF?style=flat-square&logo=github)](https://github.com/joemunene-by/GhostLM)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Ghostgim/GhostLM-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/Ghostgim/GhostLM-v0.9-experimental)

### What I ship

**AI agent safety stack**: secure-mcp, ghostguard (4-tier policy proxy with audit dashboard), CyberBench

**Defensive security toolkit**: ghostaudit (23 CIS Kubernetes checks), ghostforensics (memory forensics with YARA + Volatility + STIX 2.1 export), ghostsiem (Sigma-rule SIEM), securecommit (pre-commit secret scanner)

**Offensive tooling**: concurrent TCP port scanner, packet-level traffic analyzer, vulnerability scanner, hash-cracking framework, MAC rotator, metadata scrubber

**The ghost security suite**: eleven production CLI tools spanning recon, web and mobile scanning, ML intrusion detection, malware triage, supply chain, cloud posture, and key management (listed below)

**Full-stack platforms**: Complex Developers CRM (Next.js 15 + Prisma + Postgres), ChartSentinel (trading SaaS with Stripe + PostHog + Sentry), High-End CRM, ai-coding-assistant

</td>
<td width="50%" valign="top">

### Latest drops

**[ghostloop v1.0.3](https://github.com/joemunene-by/ghostloop)** — the agent loop, embodied. `pip install ghostloop`, 14 releases, [live HuggingFace demo](https://huggingface.co/spaces/Ghostgim/ghostloop-demo), full CI/CD with PyPI Trusted Publishing. Six simulation backends (MuJoCo / PyBullet / Gymnasium / ROS 2), 12 fail-closed policy gates, LLM + VLA policy adapters, and a bench harness with Wilson CI, McNemar, adversarial fuzzing (CMA-ES), STL temporal properties, counterfactual replay, and causal failure attribution. Production fleet dashboard with auth, rate limiting, alarms, and Prometheus. **359 tests green.**

**[ghostloop-ui](https://github.com/joemunene-by/ghostloop-ui)** — Next.js 15 + React 19 + Tailwind 4 control plane, live at [ghostloop-ui.vercel.app](https://ghostloop-ui.vercel.app). Fleet view, alarm tray, episode timeline, per-counter Prometheus metrics, and a profile-aware gamepad mapper (drone / mobile base / quadruped / arm / humanoid) built for non-coders. Demo-mode fallback keeps the deploy interactive with no backend configured.

**[ghostloop-desktop v0.2](https://github.com/joemunene-by/ghostloop-desktop)** — Tauri 2 + Rust shell wrapping ghostloop-ui as a single-file native app for macOS / Windows / Linux. Voice control, gamepad rumble on safety events (geofence block, force-cap trip, e-stop), native OS notifications, 120 Hz gamepad polling via `gilrs`, system-tray integration, and a global e-stop hotkey. Per-PR CI matrix green across all three platforms.

**[secure-mcp](https://github.com/joemunene-by/secure-mcp)** — MCP server exposing security tools to AI agents with policy gates, subprocess sandboxing, and audit trails. Fail-closed by default.

**[CyberBench](https://github.com/joemunene-by/cyberbench)** — Open, reproducible benchmark for evaluating LLMs on cybersecurity reasoning. YAML tasks, pluggable backends, ranked leaderboard.

**[linkdrop v0.7.1](https://github.com/joemunene-by/linkdrop)** — Cross-platform Tauri + Rust desktop app bridging iPhone to Linux for photos, files, notifications, screen mirroring. Daemon-backed pymobiledevice3 bridge, CI-built .deb / .AppImage.

[![ghostloop](https://img.shields.io/badge/View-ghostloop-14B8A6?style=flat-square&logo=github)](https://github.com/joemunene-by/ghostloop)
[![ghostloop-ui](https://img.shields.io/badge/View-ghostloop--ui-14B8A6?style=flat-square&logo=vercel)](https://github.com/joemunene-by/ghostloop-ui)
[![ghostloop-desktop](https://img.shields.io/badge/View-ghostloop--desktop-14B8A6?style=flat-square&logo=tauri)](https://github.com/joemunene-by/ghostloop-desktop)
[![secure-mcp](https://img.shields.io/badge/View-secure--mcp-C4A1FF?style=flat-square&logo=github)](https://github.com/joemunene-by/secure-mcp)
[![CyberBench](https://img.shields.io/badge/View-CyberBench-6C9CFF?style=flat-square&logo=github)](https://github.com/joemunene-by/cyberbench)
[![linkdrop](https://img.shields.io/badge/View-linkdrop-24C8DB?style=flat-square&logo=github)](https://github.com/joemunene-by/linkdrop)

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

<div align="center">

**Languages**<br>
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Swift](https://img.shields.io/badge/Swift-FA7343?style=flat-square&logo=swift&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Frontend, Mobile & Desktop**<br>
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=flat-square&logo=framer&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/Expo-000020?style=flat-square&logo=expo&logoColor=white)
![Tauri](https://img.shields.io/badge/Tauri-24C8DB?style=flat-square&logo=tauri&logoColor=white)
![Electron](https://img.shields.io/badge/Electron-191970?style=flat-square&logo=electron&logoColor=white)

**Backend & Data**<br>
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Bun](https://img.shields.io/badge/Bun-000000?style=flat-square&logo=bun&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![tRPC](https://img.shields.io/badge/tRPC-2596BE?style=flat-square&logo=trpc&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)

**AI / ML**<br>
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace_Hub-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Transformers](https://img.shields.io/badge/Transformers-from_scratch-EE4C2C?style=flat-square)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![MLX](https://img.shields.io/badge/MLX-Apple_Silicon-000000?style=flat-square&logo=apple&logoColor=white)
![LanceDB](https://img.shields.io/badge/LanceDB-Vector_Search-3F51B5?style=flat-square)
![MCP](https://img.shields.io/badge/MCP-Anthropic-D4A574?style=flat-square)
![FastMCP](https://img.shields.io/badge/FastMCP-D4A574?style=flat-square)
![Anthropic SDK](https://img.shields.io/badge/Anthropic_SDK-D4A574?style=flat-square&logo=anthropic&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-F55036?style=flat-square)

**Robotics, RL & Simulation**<br>
![MuJoCo](https://img.shields.io/badge/MuJoCo-DeepMind-FF6633?style=flat-square)
![PyBullet](https://img.shields.io/badge/PyBullet-Bullet_Physics-FF6633?style=flat-square)
![ROS 2](https://img.shields.io/badge/ROS_2-rclpy-22314E?style=flat-square&logo=ros&logoColor=white)
![Gymnasium](https://img.shields.io/badge/Gymnasium-Farama-0081A5?style=flat-square)
![Safe RL](https://img.shields.io/badge/Safe_RL-policy_gates-0081A5?style=flat-square)
![PPO](https://img.shields.io/badge/PPO_%2F_SAC-trainer_compat-0081A5?style=flat-square)
![VLA Models](https://img.shields.io/badge/VLA-OpenVLA_%2F_%CF%800_%2F_RT--2-14B8A6?style=flat-square)
![Sim-to-Real](https://img.shields.io/badge/Sim2Real-domain_randomization-14B8A6?style=flat-square)

**Security**<br>
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Nmap](https://img.shields.io/badge/Nmap-0E83CD?style=flat-square&logo=nmap&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=flat-square&logo=hackthebox&logoColor=white)
![Metasploit](https://img.shields.io/badge/Metasploit-2596CD?style=flat-square&logo=metasploit&logoColor=white)
![Hashcat](https://img.shields.io/badge/Hashcat-2D2D2D?style=flat-square)
![Scapy](https://img.shields.io/badge/Scapy-Packet_Crafting-339933?style=flat-square)
![YARA](https://img.shields.io/badge/YARA-00A859?style=flat-square)
![Volatility](https://img.shields.io/badge/Volatility-2D2D2D?style=flat-square)
![Sigma](https://img.shields.io/badge/Sigma_Rules-EE6600?style=flat-square)
![STIX](https://img.shields.io/badge/STIX_2.1-0066CC?style=flat-square)
![MISP](https://img.shields.io/badge/MISP-3092BD?style=flat-square)
![CIS Benchmarks](https://img.shields.io/badge/CIS_Benchmarks-C8102E?style=flat-square)
![CTF](https://img.shields.io/badge/CTF-Competitor-9FEF00?style=flat-square)

**DevOps, Observability & Quality**<br>
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Turbo](https://img.shields.io/badge/Turborepo-EF4444?style=flat-square&logo=turborepo&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-spans_%26_traces-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-%2Fmetrics-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Sentry](https://img.shields.io/badge/Sentry-362D59?style=flat-square&logo=sentry&logoColor=white)
![PostHog](https://img.shields.io/badge/PostHog-1D4AFF?style=flat-square&logo=posthog&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)

</div>

<br>

## `> git log --oneline`

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=joemunene-by&show_icons=true&hide_border=true&bg_color=0C0E14&title_color=6C9CFF&text_color=8A8FA8&icon_color=C4A1FF&ring_color=6C9CFF" height="165" />
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=joemunene-by&layout=compact&hide_border=true&bg_color=0C0E14&title_color=6C9CFF&text_color=8A8FA8" height="165" />

</div>

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=joemunene-by&bg_color=0C0E14&color=8A8FA8&line=6C9CFF&point=C4A1FF&area=true&area_color=6C9CFF&hide_border=true" width="95%" />

</div>

<br>

## `> cat README.md | tail -n 4`

<div align="center">

I'm always open to collaborating on security research, open source tooling, or interesting engineering problems.<br>
If you're building something that matters, I'd like to hear about it.

<br>

**Nairobi, Kenya** · Founder, Complex Developers · **Available for contract work** — backend builds, security reviews, API hardening · [joemunene984@gmail.com](mailto:joemunene984@gmail.com)

<br>

![Profile Views](https://komarev.com/ghpvc/?username=joemunene-by&color=6C9CFF&style=flat-square&label=Profile+Views)

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0C0E14,50:6C9CFF,100:C4A1FF&height=100&section=footer" width="100%" />

</div>
