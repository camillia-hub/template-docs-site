# Version constraints

| Component | Pinned version | Notes |
| --- | --- | --- |
| Python | 3.13 | Runs the MkDocs toolchain. |
| MkDocs | 1.6.x | With `mkdocs-material` 9.x. |
| mike | 2.x | Version publishing; CI only. |
| Markdown extensions | as configured in `mkdocs.yml` | New extensions need a docs-review discussion. |

- The strict build (`uv run mkdocs build --strict`) is the quality gate: zero
  warnings allowed.
- Theme customization stays inside `overrides/`; the theme itself is never
  forked.
