# Stack Sherpa

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Playbooks](https://img.shields.io/badge/playbooks-67-blue.svg)](SKILL.md)
[![Claude Skill](https://img.shields.io/badge/Claude-Skill-purple.svg)](https://github.com/sheikh-zain786/stack-sherpa/releases)

**A free coding skill for Claude.** One install gives Claude 67 senior-engineer playbooks covering languages, frameworks, infrastructure, security, testing, data/ML and architecture. Claude loads only the playbook it needs, so it stays fast and light.

---

## What's inside

| Area | Playbooks |
|---|---|
| **Languages** | Python, TypeScript, JavaScript, Go, Rust, Java, C#, C++, Kotlin, Swift, PHP, SQL |
| **Frameworks** | React, Next.js, Vue, Angular, NestJS, Django, FastAPI, Spring Boot, Laravel, Rails, Flutter, React Native |
| **Infrastructure** | Kubernetes, Terraform, cloud architecture, DevOps, SRE, monitoring |
| **Quality & security** | Code review, test strategy, Playwright, debugging, secure coding, security review |
| **Data & AI** | pandas, Spark, ML pipelines, RAG, fine-tuning, prompt engineering |
| **Architecture & APIs** | System design, microservices, REST/OpenAPI, GraphQL, WebSockets, MCP servers |

The full table of playbooks and their trigger phrases is in [`SKILL.md`](SKILL.md).

## How it works

`SKILL.md` is a router. When you ask Claude for coding help, it matches your request to the best playbook in `references/` and follows that playbook's workflow, checkpoints and output format.

Bigger tasks combine two or three playbooks, for example:

- **New feature:** feature-forge, architecture-designer, a framework expert, test-master
- **Bug hunt:** debugging-wizard, a framework expert, test-master, code-reviewer
- **Hardening:** secure-code-guardian, security-reviewer, test-master

## Install

### Claude (claude.ai, desktop or mobile app)

1. Download `stack-sherpa.skill` from the [Releases page](https://github.com/sheikh-zain786/stack-sherpa/releases).
2. Open **Settings → Capabilities → Skills** and upload the file.
3. Make sure Skills and code execution are turned on.

### Claude Code

```bash
git clone https://github.com/sheikh-zain786/stack-sherpa ~/.claude/skills/stack-sherpa
```

Restart Claude Code and the skill is available in every project.

## Usage

Just ask in plain language. You can also name the skill directly:

```text
/stack-sherpa review this code
```

More examples:

- "Review this pull request for bugs and security issues."
- "Design a REST API for a booking system and write the OpenAPI spec."
- "Debug this FastAPI endpoint that times out under load."
- "Write a Terraform module for a VPC with private subnets."
- "Audit this Flask app for security problems."

## Repository layout

```text
stack-sherpa/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── SKILL.md              # router with the table of all 67 playbooks
└── references/
    ├── react-expert.md
    ├── python-pro.md
    └── ...               # one file per playbook (67 total)
```

## Contributing

Issues and pull requests are welcome at
[github.com/sheikh-zain786/stack-sherpa](https://github.com/sheikh-zain786/stack-sherpa).

- Keep each playbook in `references/<name>.md`.
- When you add or rename one, update the table in `SKILL.md`.
- Keep `SKILL.md` under about 500 lines; put detail in `references/`.

## Credits and license

Released under the [MIT License](LICENSE).

Stack Sherpa is a repackaged, single-skill edition of
[Jeffallan/claude-skills](https://github.com/Jeffallan/claude-skills) (MIT).
The 67 playbooks were written by the original author. This repository merges them
into one installable skill so it fits Claude's upload limits and installs in one step.

- Repackaging and router: Copyright (c) 2026 sheikh-zain786
- Original playbooks: Copyright their respective author

Both notices must stay in the `LICENSE` file when you copy or modify this project.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).
