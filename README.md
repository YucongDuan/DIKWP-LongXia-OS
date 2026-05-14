# DIKWP LongXia OS

**DIKWP LongXia OS** is an offline-first, GitHub-ready open-source semantic exoskeleton for Chinese DeepSeek users.

LongXia (龙虾) means: a small user with a hard semantic shell and two claws. The shell protects intent, evidence, privacy, and boundaries. The claws compile better prompts and audit model answers.

This project does **not** bypass DeepSeek access rules, account limits, safety policies, paid plans, or compute quotas. It helps users prepare better prompts, compress context, preserve purpose, and repair weak answers when using any legally available DeepSeek interface.

## Core idea

AI access may become uneven. Some users will have high-end models, long context, tools, and enterprise privileges; others will have limited access. LongXia OS gives users a portable semantic capsule:

- DIKWP task registration: Data / Information / Knowledge / Wisdom / Purpose / Reliability.
- DeepSeek prompt pack: Think / Non-Think modes, Chinese-friendly task phrasing, evidence boundary, output structure.
- Micro capsule: low-token context for constrained chats.
- Answer audit: unsupported certainty, missing residual, missing evidence, boundary gaps, sensitive claims, overlong output.
- Model route plan: choose economical, reasoning, or long-context paths without hard-coding any provider dependency.
- No telemetry, no network core, no API key capture.

## Install

```bash
pip install -e .
```

## Build a semantic capsule

```bash
longxia build examples/sample_chinese_task.json --out outputs/demo
```

## Audit an answer

```bash
longxia audit examples/sample_deepseek_answer.md --capsule outputs/demo/semantic_capsule.json --out outputs/demo
```

## Static audit

```bash
longxia static-audit src --out outputs/demo/static_boundary_audit_report.json
```

## Outputs

- `semantic_capsule.json`
- `deepseek_attachment_prompt.md`
- `micro_capsule.txt`
- `model_route_plan.json`
- `answer_audit_report.json`
- `answer_repair_plan.md`
- `static_boundary_audit_report.json`

## Boundary

LongXia OS is for semantic clarity, evidence discipline, and answer repair. It is not a jailbreaking tool and must not be used to extract hidden prompts, evade platform policies, bypass authentication, or obtain paid capabilities without authorization.
