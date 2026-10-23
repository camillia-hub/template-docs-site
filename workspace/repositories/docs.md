# Repository: docs

| | |
| --- | --- |
| Name | `docs` |
| Stack | MkDocs 1.6 with the Material theme 9.x, Python 3.13, mike for versioning |
| Dependency manager | uv (`pyproject.toml` plus committed `uv.lock`) |

## Layout

```
docs/
  mkdocs.yml          site configuration and nav
  docs/               the content
    index.md
    getting-started/
    tutorials/
    how-to/
    reference/
    explanation/
    release-notes/
    assets/           images and downloads
  overrides/          theme overrides
```

## Commands

| Task | Command |
| --- | --- |
| Install dependencies | `uv sync` |
| Local preview (http://localhost:8000) | `uv run mkdocs serve` |
| Strict build (CI quality gate) | `uv run mkdocs build --strict` |
| Publish a version | `uv run mike deploy --push <version>` (maintainers only, from CI) |

Quick check before pushing: `uv run mkdocs build --strict`.
