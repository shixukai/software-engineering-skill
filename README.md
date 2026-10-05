<p align="center">
  <img src="assets/hero.svg" alt="Software Engineering: task-led guidance for AI coding agents" width="100%" />
</p>

<p align="center">
  <strong>Make engineering decisions traceable to evidence.</strong><br />
  An experimental Chinese-language software engineering Skill for AI coding agents.
</p>

<p align="center">
  <a href="#project-status">Project status</a> ·
  <a href="#workflow-preview">Watch the preview</a> ·
  <a href="#scope">Scope</a> ·
  <a href="README.zh-CN.md">简体中文</a>
</p>

> **Project preview.** This repository currently contains an introduction and original demonstration assets. The installable Skill runtime has not been published here.

## The idea

Start with the engineering question. Inspect the relevant requirements, code or observations. Select a method that fits the evidence, explain the trade-offs, and state what was actually verified.

The Skill under development organizes its guidance around tasks, so an agent can read a relevant workflow and method instead of loading an entire reference collection. Its intended output is a concrete decision, the evidence behind it, and any unresolved limits.

- **Clear assumptions:** separate confirmed facts, constraints and unknowns
- **Task-specific guidance:** choose the depth and method for the actual problem
- **Reviewable conclusions:** identify evidence, verification scope and remaining risk

## Workflow preview

This original 27-second animation illustrates the intended interaction. It is not a recording of a working installation, a benchmark or a real project result.

https://github.com/user-attachments/assets/3a075073-f99e-46dc-869e-ce11d510254d

## Scope

The runtime being prepared covers ten task workflows:

- Requirements clarification and acceptance
- Architecture, domain and integration design
- Implementation changes
- Code and change review
- Testing strategy and verification
- Defect diagnosis
- Refactoring and legacy changes
- Integration, build and delivery
- Reliability and operations
- Engineering planning and collaboration

These are guidance areas, not a claim that every engineering capability has been validated. The Skill grants no additional authority to edit, publish or operate a system.

## Project status

The installable runtime is being held until its applicable publication checks are complete. There is currently no `SKILL.md` or installation command in this repository.

Completed preparation includes a separate distribution boundary, source-attribution review, and static file, link and routing checks on the candidate. Final runtime behavior and host-discovery checks have not been completed. Real-world engineering impact has not been evaluated.

We do not claim proven improvements in quality, speed or cost. See [STATUS.md](STATUS.md) for the current boundary.

## License and feedback

Original introduction text and presentation assets in this repository are available under the [MIT License](LICENSE). Third-party works are not relicensed; see [NOTICE.md](NOTICE.md).

Issues are welcome for questions and specific feedback on the project direction. Use original fictional examples. Do not post private source code, production logs, personal information or copyrighted source passages.
