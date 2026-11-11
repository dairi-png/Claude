# Claude

This repo enables the [OpenAI Codex plugin for Claude Code](https://github.com/openai/codex-plugin-cc) at project level via `.claude/settings.json`.

## First run

1. Open Claude Code in this repo and accept the prompt to install `codex@openai-codex`.
2. Run `/reload-plugins`, then `/codex:setup`.
3. If Codex is not logged in, run `!codex login` (ChatGPT account or OpenAI API key).

Requires Node.js 18.18+. Usage counts against your Codex limits.

## Commands

| Command | What it does |
|---|---|
| `/codex:review` | Read-only Codex review of uncommitted changes, or `--base main` for a branch |
| `/codex:adversarial-review` | Review that challenges design choices; accepts focus text |
| `/codex:rescue` | Hands a task (bug hunt, fix) to Codex |
| `/codex:transfer` | Moves this Claude session into a resumable Codex thread |
| `/codex:status` / `/codex:result` / `/codex:cancel` | Manage background jobs |

Leave the review gate (`/codex:setup --enable-review-gate`) off unless you are watching the session: it can loop and drain usage.
