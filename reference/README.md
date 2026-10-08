# reference/

This directory is intentionally empty in the repo. The full ASD-STE100 specification is copyrighted by ASD and is not redistributed here.

On your local machine, put the spec at `~/.claude/reference/`:

```
~/.claude/reference/
├── ASD-STE100_Issue9.pdf    # the official PDF
└── ASD-STE100_Issue9.txt    # the grep-friendly extraction
```

See the root `README.md` for the one-shot setup commands.

The `CLAUDE.md` in this repo tells Claude Code to grep `~/.claude/reference/ASD-STE100_Issue9.txt` whenever an in-session substitution is uncertain. Without the extraction in place, Claude falls back to the inline tables only.
