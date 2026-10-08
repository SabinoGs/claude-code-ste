# reference/

Files that `CLAUDE.md` points to for in-session lookups.

## In the repo

- `ASD-STE100_Issue9.txt` — grep-friendly text extraction of the full ASD-STE100 Issue 9 specification (pages marked with `===PAGE N===`). Claude Code greps this file when a specific word is not in the inline tables of `CLAUDE.md`.

## Not in the repo

- `ASD-STE100_Issue9.pdf` — the original PDF. Not shipped here. Download the official file from <https://www.asd-ste100.org/assets/files/ASD-STE100_ISSUE9.pdf> if you want it on disk.

## Local install location

Install both files at `~/.claude/reference/` (that is the path `CLAUDE.md` references):

```
~/.claude/reference/
├── ASD-STE100_Issue9.pdf    # optional
└── ASD-STE100_Issue9.txt    # required for grep lookups
```

See the root `README.md` for the install commands.

## Copyright

The content of `ASD-STE100_Issue9.txt` is a derivative of material copyrighted by the AeroSpace and Defence Industries Association of Europe (ASD). Use the file for personal reference. For publication or redistribution, go to the official source.
