# claude-code-ste

Global writing style for [Claude Code](https://claude.com/claude-code), based on **ASD-STE100 Simplified Technical English (Issue 9, 2025-01-15)**.

Drop `CLAUDE.md` into `~/.claude/` and the text extraction into `~/.claude/reference/`. Every Claude Code session on the machine then writes in STE for chat replies, code comments, commit messages, PRs, error messages, and ticket replies.

## What is in here

- `CLAUDE.md` — the authoritative writing style. All 9 STE rule sections distilled, the 8 General Recommendations, STE's own "List of recurring errors" (expanded with software-writing offenders), the full 240-verb approved-verb list, a 15-item self-check, and before/after examples.
- `reference/ASD-STE100_Issue9.txt` — grep-friendly extraction of the full spec (text only, with `===PAGE N===` markers). `CLAUDE.md` tells Claude Code to grep this file when an in-session substitution is uncertain.
- `reference/README.md` — notes about the reference files.

The ASD-STE100 PDF itself is **not** in this repo. Download it from the official source if you want it (see below).

## Install

```sh
# From the repo root
mkdir -p ~/.claude/reference

# The style
cp CLAUDE.md ~/.claude/CLAUDE.md

# The grep-friendly spec extraction
cp reference/ASD-STE100_Issue9.txt ~/.claude/reference/ASD-STE100_Issue9.txt
```

Prefer symlinks if you want `git pull` to keep the installed copies up to date:

```sh
ln -sf "$PWD/CLAUDE.md" ~/.claude/CLAUDE.md
ln -sf "$PWD/reference/ASD-STE100_Issue9.txt" ~/.claude/reference/ASD-STE100_Issue9.txt
```

Verify a lookup:

```sh
grep -i "^perform" ~/.claude/reference/ASD-STE100_Issue9.txt
```

### Optional — the original PDF

```sh
curl -L -A "Mozilla/5.0" \
  -o ~/.claude/reference/ASD-STE100_Issue9.pdf \
  https://www.asd-ste100.org/assets/files/ASD-STE100_ISSUE9.pdf
```

## Scope

The style applies to: chat replies, code comments and docstrings, commits, PR titles and bodies, PR review comments, error messages, Jira/Linear/Slack/GitHub/Gmail replies.

The style does **not** apply to: code identifiers, quoted user text, log strings that match existing infrastructure, third-party API payloads, values that must match an external schema or a test fixture.

In an existing document with a different style, match the in-file style first.

## Register

Apply STE in every Claude Code session, including chat with the user. The grammar rules and the vocabulary rule hold in every register. Do not relax the style because the user writes casually.

## Precedence

The file states its own precedence over any project-level `CLAUDE.md` style guidance. A project `CLAUDE.md` may still set role, architecture, or domain context — but writing style defers to this file.

## Source

ASD-STE100 is a controlled natural language developed by the AeroSpace and Defence Industries Association of Europe (ASD) and the STEMG. Official site: <https://www.asd-ste100.org>.

The `reference/ASD-STE100_Issue9.txt` file in this repo is a mechanical text extraction of the freely-downloadable official PDF, included so Claude Code can grep for word-level substitutions without a separate download step. It is a derivative work of material that is copyrighted by ASD; use it under fair-use terms for personal reference. For publication, authoritative citation, or redistribution, go to the official source.

## License

MIT for the compact `CLAUDE.md` rendition, the setup scripts, and the examples. The ASD-STE100 specification itself (including the content of `reference/ASD-STE100_Issue9.txt`) is **not** covered by this license and remains the intellectual property of ASD.
