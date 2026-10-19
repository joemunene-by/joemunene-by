<div align="center">

# Joe Munene

**Founder, [Complex Developers](https://github.com/complexdevelopers) · Nairobi, Kenya**

I build security-focused AI systems end to end: language models trained from scratch, the agent runtimes that make them safe to deploy, and the security tooling around them.

[![ghostloop](https://img.shields.io/pypi/v/ghostloop?style=flat-square&label=ghostloop&color=1f2328)](https://pypi.org/project/ghostloop/)
[![ghostprobe](https://img.shields.io/pypi/v/ghostprobe?style=flat-square&label=ghostprobe&color=1f2328)](https://pypi.org/project/ghostprobe/)
[![GhostLM on Hugging Face](https://img.shields.io/badge/GhostLM-Hugging%20Face-1f2328?style=flat-square)](https://huggingface.co/Ghostgim/GhostLM-v0.9-experimental)
[![Portfolio](https://img.shields.io/badge/Portfolio-1f2328?style=flat-square)](https://my-portfolio-peach-eta-42.vercel.app)
[![Email](https://img.shields.io/badge/Email-1f2328?style=flat-square)](mailto:joemunene984@gmail.com)

</div>

## About

I am the founder of [Complex Developers](https://github.com/complexdevelopers), a software studio in Nairobi, and a Computer Science student at Moi University. My work centers on systems that stay auditable under adversarial conditions, from model internals through to the agent runtime that executes their decisions. The [studio's platform and CRM](https://github.com/complexdevelopers/Complex-Developers-Web) runs on Next.js, Prisma, and Postgres.

Alongside the studio I have trained a cybersecurity language model from scratch, published a fail-closed agent safety runtime to PyPI, and contributed fixes upstream to PyTorch and AutoGPT. I prefer to demonstrate engineering with working, tested code, which is what the rest of this page points to.

## Open source contributions

- **[AutoGPT #12805](https://github.com/Significant-Gravitas/AutoGPT/pull/12805)** (merged): fixed agent-name preservation in `AgentExecutor` node titles after a page reload in the visual builder, so a saved graph reopens with its node names intact.
- **[pytorch/ignite #3750](https://github.com/pytorch/ignite/pull/3750)** (open, under review): adds `WelfordVariance` and `WelfordCovariance`, shared running-statistics primitives built on Welford's online algorithm with the Chan parallel merge for cross-rank reduction, so variance and correlation stay numerically stable where the naive `E[X^2] - E[X]^2` formula cancels at large means. It underpins the `PearsonCorrelation` fix in [#3741](https://github.com/pytorch/ignite/pull/3741).
- **[OWASP Cheat Sheet Series #2111](https://github.com/OWASP/CheatSheetSeries/pull/2111)**: proposed guidance on AI model supply-chain security, covering serialization risks in model artifacts and provenance verification, revised through maintainer review.

## Selected projects

### GhostLM

An open source cybersecurity language model built from scratch in PyTorch. An 81M-parameter decoder-only transformer (RoPE, SwiGLU, RMSNorm) trained on a 422M-token corpus drawn from 27 sources, including security writeups, NVD CVEs, MITRE, CWE, OWASP, NIST SP 800, FineWeb-Edu, and open source code across 15 languages. It ships a tool-using agent runtime, a multi-vendor HTTP server speaking the OpenAI, Anthropic, Gemini, and Ollama wire formats, an MCP server, and a packaged evaluation suite that reports Wilson confidence intervals and McNemar paired comparisons. [Repository](https://github.com/joemunene-by/GhostLM).

### ghostloop

A fail-closed safety runtime for embodied agents, on PyPI as `ghostloop`, with a [live demo on Hugging Face](https://huggingface.co/spaces/Ghostgim/ghostloop-demo). Six simulation backends (MuJoCo, PyBullet, Gymnasium, ROS 2), twelve fail-closed policy gates, LLM and VLA policy adapters, and a benchmark harness with adversarial fuzzing, temporal-property checks, counterfactual replay, and causal failure attribution. A [Next.js control plane](https://github.com/joemunene-by/ghostloop-ui) and a [Tauri desktop app](https://github.com/joemunene-by/ghostloop-desktop) wrap it for fleet operation, both green on CI.

### ghostprobe

A dynamic red-team probe for MCP servers, mapped to the OWASP MCP Top 10, on PyPI as `ghostprobe`. It finds tool poisoning, hidden-instruction smuggling, and lethal-trifecta exposure through static analysis, and adds a live canary that plants a marker, calls a server's read-only tools, and scans the real output for prompt injection and cross-tool data capture over both stdio and HTTP/SSE transports. 82 tests, released through PyPI Trusted Publishing. [Repository](https://github.com/joemunene-by/ghostprobe).

### secure-mcp and CyberBench

[secure-mcp](https://github.com/joemunene-by/secure-mcp) exposes security tools to AI agents behind policy gates, subprocess sandboxing, and audit trails, fail-closed by default. [CyberBench](https://github.com/joemunene-by/cyberbench) is an open, reproducible benchmark for evaluating language models on cybersecurity reasoning, with YAML-defined tasks, pluggable backends, and a ranked leaderboard.

Other work includes ghostguard (a four-tier policy proxy with an audit dashboard), ghostforensics, ghostsiem, and ghostaudit on the security side, linkdrop (an iPhone-to-Linux continuity app on Tauri and Rust), and full-stack products including the Complex Developers CRM and ChartSentinel, a trading analytics platform.

## The ghost security suite

Eleven command-line security tools, shipped as one suite. Each is installable, test-covered, and green on GitHub Actions across Python 3.11 and 3.12, with console, JSON, and SARIF output for CI gating and authorized-use framing throughout.

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

## Skills

**Systems and AI.** Python and PyTorch, including transformers written from scratch: training, tokenization, and evaluation with proper statistics. Rust, TypeScript, and C. MCP servers and multi-vendor LLM serving.

**Security.** Offensive work (recon, web and mobile scanning, exploitation tooling) and defensive work (intrusion detection, malware triage, SIEM, memory forensics, cloud posture, key management). YARA, Sigma, STIX, and CIS benchmarks.

**Product.** Full-stack web (Next.js, React, Tailwind, Postgres, Prisma), cross-platform desktop (Tauri, Rust), and mobile (React Native, shipped to the Google Play Store).

**Infrastructure.** Docker, Kubernetes, Terraform, GitHub Actions, Prometheus, and CI/CD with PyPI Trusted Publishing.

## Writing

Longer technical pieces live in [joemunene-by/writing](https://github.com/joemunene-by/writing). The most developed is [AI Model Supply Chain Security](https://github.com/joemunene-by/writing/blob/main/ai-model-supply-chain-security.md), on serialization risks in model artifacts (pickle and `.pt` code execution, safetensors and ONNX alternatives), provenance verification, artifact scanning, and model bills of materials. It was proposed to the OWASP Cheat Sheet Series and revised through maintainer review.

## Now

Training ghost-base, the successor to GhostLM at about 360M parameters, on rented GPU. Available for select work in backend systems, security reviews, and API hardening.

**Joe Munene** · Founder, Complex Developers · Nairobi, Kenya · [joemunene984@gmail.com](mailto:joemunene984@gmail.com)
