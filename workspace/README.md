# Documentation workspace: MkDocs Material

This workspace produces the **{{ projectName }}** documentation site: a docs-as-code product
built with MkDocs Material, versioned and published from CI (see
`repositories/docs.md`).

## How the agent should navigate this workspace

Read in this order before your first task:

1. `rules/` — mandatory editorial rules: `writing-style.md` (how text reads) and
   `structure.md` (where content lives). Rules win over conventions when they
   conflict.
2. `conventions/` — navigation, commit style and the review checklist every
   change must pass.
3. `camflows/` — the workspace's own `docs-review` camflow plus its event binding
   in `triggers.camflow.yaml`; it reviews docs changes like an editor.
4. `repositories/docs.md` — the repository layout and every build command. The
   strict build listed there is the quality gate.
5. `business/` — the docs vocabulary (`glossary.md`) and the content policy
   (`rules.md`).
6. `architecture/components.md` — what the docs platform consists of.
7. `technical/constraints/versions.md` — pinned toolchain versions.
8. `ui/map.md` — the site map; keep it in sync when sections change.

When a task teaches you a durable fact about the content or its audience, record
it in `business/` — not only in the task paper.
