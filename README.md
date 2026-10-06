<p align="center">
  <img src="assets/hero.svg" alt="Software Engineering: task-led guidance for AI coding agents" width="100%" />
</p>

<p align="center">
  <strong>Make engineering decisions traceable to evidence.</strong><br />
  An experimental Chinese-language software engineering Skill for AI coding agents.
</p>

<p align="center">
  <a href="#try-the-installation-preview">Try the preview</a> ·
  <a href="#project-status">Project status</a> ·
  <a href="#workflow-preview">Watch the preview</a> ·
  <a href="#scope">Scope</a> ·
  <a href="README.zh-CN.md">简体中文</a>
</p>

> **Installation preview · `0.1.0-preview.1`.** An experimental, locally installable Skill package. Final host loading and model-behavior checks are incomplete; start in a disposable practice directory.

## The idea

Start with the engineering question. Inspect the relevant requirements, code or observations. Select a method that fits the evidence, explain the trade-offs, and state what was actually verified.

The experimental Skill organizes its guidance around tasks, so an agent can read a relevant workflow and method instead of loading an entire reference collection. Its intended output is a concrete decision, the evidence behind it, and any unresolved limits.

- **Clear assumptions:** separate confirmed facts, constraints and unknowns
- **Task-specific guidance:** choose the depth and method for the actual problem
- **Reviewable conclusions:** identify evidence, verification scope and remaining risk

## Workflow preview

This original 27-second animation illustrates the intended interaction. It is not a recording of a working installation, a benchmark or a real project result.

https://github.com/user-attachments/assets/3a075073-f99e-46dc-869e-ce11d510254d

## Scope

The preview runtime covers ten task workflows:

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

## Try the installation preview

**Version: `0.1.0-preview.1` (pre-release).** The [Skill entry](skills/software-engineering/SKILL.md) and its references are included for local experimentation. Static package checks have passed; successful loading and model behavior in a host have not been verified for this public package.

Download this version's source archive or check out its tag, then open a terminal at the repository root. These commands require an installed Codex CLI and Bash or Zsh on macOS/Linux:

```bash
preview_dir="$(mktemp -d "${TMPDIR:-/tmp}/se-skill-preview.XXXXXX")" &&
mkdir -p "$preview_dir/.agents/skills" &&
cp -R skills/software-engineering "$preview_dir/.agents/skills/" &&
printf 'Preview directory: %s\n' "$preview_dir" &&
(cd "$preview_dir" && codex)
```

Keep that terminal open and the printed path. The copy is project-local; it does not install the Skill in your home directory or edit global configuration. Directory separation is not a security sandbox: your host's existing settings, other skills, connections and approval rules still apply.

Inside Codex, use `/skills` or explicitly mention `$software-engineering`. Start with a fictional, non-sensitive analysis task:

```text
$software-engineering
A fictional report job may finish after a user clicks Cancel.
List the missing behavioral requirements and observable acceptance conditions.
Analysis only: do not modify files or call external services.
```

Select the entry under the printed preview directory if another Skill has the same name. If it does not appear, restart Codex and check the [official Skill documentation](https://learn.chatgpt.com/docs/build-skills). Other hosts have not been verified. Keep the complete Skill folder; copying only `SKILL.md` breaks its references.

### Remove the preview

Exit Codex first. In the same terminal, move only this copied Skill out of its discovery path:

```bash
if [ -n "${preview_dir:-}" ] &&
   [ -f "$preview_dir/.agents/skills/software-engineering/SKILL.md" ] &&
   [ ! -e "$preview_dir/software-engineering.disabled" ]; then
  mv "$preview_dir/.agents/skills/software-engineering" \
     "$preview_dir/software-engineering.disabled"
fi
```

Restart the host before checking that this local entry is gone. The moved copy remains recoverable. After saving any practice work you want to keep, you can delete the printed temporary directory manually. No global Skill or configuration needs to be removed.

## Project status

This pre-release makes the runtime available for local installation experiments before full acceptance. It is not a stable release, and publication does not mean its remaining checks have passed.

Completed preparation includes a separate distribution boundary, source-attribution review, and static file, link and routing checks on the candidate. Final runtime behavior and host-discovery checks have not been completed. Real-world engineering impact has not been evaluated.

We do not claim proven improvements in quality, speed or cost. See [STATUS.md](STATUS.md) for the current boundary.

## License and feedback

Original Skill text, introduction text and presentation assets in this repository are available under the [MIT License](LICENSE). Third-party works are not relicensed; see [NOTICE.md](NOTICE.md).

Issues are welcome for questions and specific feedback on the project direction. Use original fictional examples. Do not post private source code, production logs, personal information or copyrighted source passages.
