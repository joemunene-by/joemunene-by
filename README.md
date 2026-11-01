# Joe Munene

Founder of [Complex Developers](https://github.com/complexdevelopers), a software studio in Nairobi. I build security tooling and the AI systems around it: a language model trained from scratch, a fail-closed runtime for the agents that use it, and scanners for the surfaces they expose.

[![ghostloop](https://img.shields.io/pypi/v/ghostloop?style=flat-square&label=ghostloop&color=1f2328)](https://pypi.org/project/ghostloop/)
[![ghostprobe](https://img.shields.io/pypi/v/ghostprobe?style=flat-square&label=ghostprobe&color=1f2328)](https://pypi.org/project/ghostprobe/)

## Work

**[GhostLM](https://github.com/joemunene-by/GhostLM)**. A cybersecurity language model built from scratch in PyTorch, and the system around it: a corpus pipeline over 27 sources (CVE, MITRE, CWE, OWASP, NIST, security writeups, code in 15 languages), PyTorch and MLX trainers, an evaluation suite that reports Wilson intervals and McNemar paired comparisons, a tool-using agent runtime, and a server that speaks the OpenAI, Anthropic, Gemini and Ollama wire formats. The published model is on [Hugging Face](https://huggingface.co/Ghostgim/ghost-small-gen).

**[ghostloop](https://github.com/joemunene-by/ghostloop)**. A fail-closed safety runtime for embodied agents. Six simulation backends (MuJoCo, PyBullet, Gymnasium, ROS 2), twelve policy gates that refuse on any exception, LLM and VLA policy adapters, and a benchmark harness with adversarial fuzzing, counterfactual replay and causal failure attribution. On PyPI, with a [live demo](https://huggingface.co/spaces/Ghostgim/ghostloop-demo).

**[ghostprobe](https://github.com/joemunene-by/ghostprobe)**. A dynamic red-team probe for MCP servers covering all ten categories of the OWASP MCP Top 10. Beyond static checks it plants a canary, calls the server's read-only tools over stdio or HTTP, and scans the real output for prompt injection and cross-tool data capture. On PyPI through Trusted Publishing.

**[secure-mcp](https://github.com/joemunene-by/secure-mcp)**. The other side of the same problem: an MCP server that exposes security tools to agents behind policy gates, subprocess sandboxing and an audit trail.

The [ghostsuite](https://github.com/joemunene-by/ghostsuite) collects eleven smaller command-line tools (recon, web and mobile scanning, malware triage, SBOM and CVE scanning, cloud posture, key management), each with tests, CI on Python 3.11 and 3.12, and SARIF output. [ghostsoc](https://github.com/joemunene-by/ghostsoc) drives them together and writes one ranked report.

## Upstream

- [AutoGPT #12805](https://github.com/Significant-Gravitas/AutoGPT/pull/12805), merged: agent names in `AgentExecutor` nodes survive a reload of the visual builder.
- [pytorch/ignite #3750](https://github.com/pytorch/ignite/pull/3750), in review: `WelfordVariance` and `WelfordCovariance`, running statistics with the Chan parallel merge for cross-rank reduction, so variance stays stable where `E[X^2] - E[X]^2` cancels. Underpins the `PearsonCorrelation` fix in [#3741](https://github.com/pytorch/ignite/pull/3741).
- [OWASP Cheat Sheet Series #2111](https://github.com/OWASP/CheatSheetSeries/pull/2111): a proposed cheat sheet on AI model supply-chain security, revised through maintainer review. The text lives in [writing](https://github.com/joemunene-by/writing/blob/main/ai-model-supply-chain-security.md).

## Stack

Python and PyTorch for models and tooling, Rust and Tauri for desktop, TypeScript with Next.js and Postgres for product work, GitHub Actions for CI.

Open to backend and security work. [joemunene984@gmail.com](mailto:joemunene984@gmail.com)
