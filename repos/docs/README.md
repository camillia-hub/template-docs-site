# {{ projectName }} — Docs

MkDocs Material documentation site for **{{ projectName }}**, versioned and
published from CI.

## Layout

- `docs/` — the content tree, organised per the Diataxis sections in the
  workspace's `rules/structure.md`
- `mkdocs.yml` — site configuration and navigation

## Commands

```bash
pip install -r requirements.txt
mkdocs serve
mkdocs build --strict
```

The strict build is the quality gate: the workspace contract
(`repositories/docs.md`) makes it the check the agent runs before calling a
docs change done.
