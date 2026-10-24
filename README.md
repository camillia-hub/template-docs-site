# MkDocs Documentation Site — Camillia workspace template

A Camillia Community Hub workspace template for teams running a docs-as-code
product site on MkDocs Material. Ships with an editorial docs-review camflow that
checks changes against the style rules and the strict build.

## What's inside

The `workspace/` directory is the template's `.workspace` contract tree:

```
workspace/
  README.md                     workspace overview and agent navigation guide
  rules/
    writing-style.md            voice, tense, runnable samples, spelling
    structure.md                Diataxis sections, nav, front matter, links
  conventions/
    navigation.md               nav sections, ordering, release notes
    commits.md                  scoped docs commits and PR previews
    review-checklist.md         what a docs review verifies
  camflows/
    docs-review.camflow.yaml    custom camflow: build + editorial review
    triggers.camflow.yaml       binds docs.review-requested to the camflow
  repositories/
    docs.md                     repo descriptor: layout, mkdocs commands
  business/
    glossary.md                 docs vocabulary skeleton
    rules.md                    content policy skeleton
  architecture/
    components.md               docs platform components
  technical/constraints/
    versions.md                 pinned MkDocs/Material versions, strict build
  ui/
    map.md                      site map (top-level navigation)
```

Two payload areas have special meaning to the product rather than to the
workspace tree: `template.json` declares the expected repositories (see
[Template contract](#template-contract)), and `repos/` carries the seed
content the wizard applies to them (`docs`).

## How to use

Install from the Camillia Community Hub, then create a workspace from this
template. Camillia installs the `workspace/` tree as the new workspace's
`.workspace` contract: the agent reads these rules, conventions, camflow
bindings, repository descriptors and docs skeletons before every task. Where
the workspace files carry `{{ projectName }}` or `{{ orgName }}` tokens, they
are substituted with your project and organization names when the template is
applied — no manual placeholder hunt. After installation, adapt the section
names, site metadata and pinned versions to your product.

## Template contract

`template.json` declares the repositories this product is made of; the
workspace wizard walks each one and offers to **create** a fresh repo at your
git provider or **load** an existing one:

| Key | Label | Description | Required | Override default |
|---|---|---|---|---|
| `docs` | Documentation site | MkDocs documentation site | yes | no |

Seed content for each repo lives under `repos/<key>/` (a starter README and
`.gitignore`). Applying a seed to a repo that already has content requires the
"authorize content override" choice in the wizard; before anything is
overwritten the current branch heads are tagged
`camillia-backup/template-<yyyyMMdd-HHmmss>`, so existing work is never lost.

Replacement tokens — `{{ orgName }}`, `{{ projectName }}` and `{{ projectId }}`
— are substituted across all workspace-bound files at apply time. See the
[extension guidelines](https://github.com/camillia-hub/extension-guidelines)
for the full template contract.

## License

MIT — see [LICENSE](LICENSE).
