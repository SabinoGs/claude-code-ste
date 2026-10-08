# claude-code-ste

Global writing style for [Claude Code](https://claude.com/claude-code), based on **ASD-STE100 Simplified Technical English (Issue 9, 2025-01-15)**.

Drop `CLAUDE.md` into `~/.claude/` to force every Claude Code session on the machine to write in STE for chat replies, code comments, commit messages, PRs, error messages, and ticket replies.

## What is in here

- `CLAUDE.md` — the authoritative writing style. All 9 STE rule sections distilled, the 8 General Recommendations, STE's own "List of recurring errors" (expanded with software-writing offenders), the full 240-verb approved-verb list, a 15-item self-check, and before/after examples.
- `reference/README.md` — tells you where to put the full STE spec on your local machine for `grep` lookups.

The full STE spec is **not** in this repo (it is copyrighted by ASD and must come from the official source).

## Install

```sh
# From the repo root
cp CLAUDE.md ~/.claude/CLAUDE.md
# or symlink if you want pulls to update it automatically
ln -sf "$PWD/CLAUDE.md" ~/.claude/CLAUDE.md
```

Then download the official spec once for in-session `grep` lookups:

```sh
mkdir -p ~/.claude/reference
curl -L -A "Mozilla/5.0" \
  -o ~/.claude/reference/ASD-STE100_Issue9.pdf \
  https://www.asd-ste100.org/assets/files/ASD-STE100_ISSUE9.pdf
```

For `grep`-friendly lookups, also extract the text (needs `pypdf` and `cryptography`):

```sh
python3 -m venv /tmp/pdfvenv
/tmp/pdfvenv/bin/pip install pypdf cryptography
/tmp/pdfvenv/bin/python - <<'PY'
from pypdf import PdfReader
r = PdfReader('/Users/'+__import__('os').environ['USER']+'/.claude/reference/ASD-STE100_Issue9.pdf')
with open('/Users/'+__import__('os').environ['USER']+'/.claude/reference/ASD-STE100_Issue9.txt','w') as f:
    for i,p in enumerate(r.pages,1):
        f.write(f'\n===PAGE {i}===\n'); f.write(p.extract_text() or '')
PY
```

Now Claude Code can look up any word that is not in the inline tables:

```sh
grep -i "^perform" ~/.claude/reference/ASD-STE100_Issue9.txt
```

## Scope

The style applies to: chat replies, code comments and docstrings, commits, PR titles and bodies, PR review comments, error messages, Jira/Linear/Slack/GitHub/Gmail replies.

The style does **not** apply to: code identifiers, quoted user text, log strings that match existing infrastructure, third-party API payloads, values that must match an external schema or a test fixture.

In an existing document with a different style, match the in-file style first.

## Register

Mirror the user's register in casual chat. Keep the grammar rules in every register. Relax the vocabulary rule only in casual chat.

## Precedence

The file states its own precedence over any project-level `CLAUDE.md` style guidance. A project `CLAUDE.md` may still set role, architecture, or domain context — but writing style defers to this file.

## Source

ASD-STE100 is a controlled natural language developed by the AeroSpace and Defence Industries Association of Europe (ASD) and the STEMG. Official site: <https://www.asd-ste100.org>.

This repo is a compact derivative for personal use with Claude Code. It is not a replacement for the spec and is not endorsed by ASD.

## License

MIT for the files in this repo (the compact rendition, examples, and setup scripts). The ASD-STE100 specification itself is **not** covered by this license and is owned by ASD. Download the spec only from the official source.
