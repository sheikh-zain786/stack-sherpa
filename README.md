# Stack Sherpa

Free coding skill for Claude. One install gives Claude 67 senior-engineer
playbooks covering languages, frameworks, infrastructure, security, testing,
data/ML and architecture. Claude loads only the playbook it needs, so it
stays fast and light.

## What's inside

- **Languages:** Python, TypeScript, JavaScript, Go, Rust, Java, C#, C++, Kotlin, Swift, PHP, SQL
- **Frameworks:** React, Next.js, Vue, Angular, NestJS, Django, FastAPI, Spring Boot, Laravel, Rails, Flutter, React Native
- **Infrastructure:** Kubernetes, Terraform, cloud architecture, DevOps, SRE, monitoring
- **Quality & security:** code review, test strategy, Playwright, debugging, secure coding, security review
- **Data & AI:** pandas, Spark, ML pipelines, RAG, fine-tuning, prompt engineering
- **Architecture & APIs:** system design, microservices, REST/OpenAPI, GraphQL, WebSockets, MCP servers

See `SKILL.md` for the full table of playbooks and their triggers.

## How it works

`SKILL.md` is a router. When you ask for coding help, Claude matches your
request to the best playbook in `references/` and follows its workflow.
Complex tasks combine two or three playbooks, for example
feature-forge + architecture-designer + a framework expert + test-master.

## Install

**Claude (claude.ai / desktop app):**
1. Download `stack-sherpa.skill` (or the zip) from the Releases page.
2. Open Settings → Capabilities → Skills and upload the file.
3. Make sure Skills / code execution is enabled.

**Claude Code:**
```bash
git clone https://github.com/<your-username>/stack-sherpa ~/.claude/skills/stack-sherpa
```

## Example prompts

- "Review this pull request for bugs and security issues."
- "Design a REST API for a booking system and write the OpenAPI spec."
- "Debug this FastAPI endpoint that times out under load."
- "Write a Terraform module for a VPC with private subnets."

## Credits and license

MIT licensed. Stack Sherpa is a repackaged, single-skill version of
[Jeffallan/claude-skills](https://github.com/Jeffallan/claude-skills)
(MIT). The 67 playbooks were written by the original author. This repo
merges them into one installable skill so it fits upload limits.

Copyright (c) 2026 <your name>, for the repackaging.
Original work copyright its respective author. See LICENSE.

## Contributing

Issues and pull requests welcome. Please keep each playbook in
`references/<name>.md` and update the table in `SKILL.md` when adding one.
