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

## How to use

Install from the Camillia Community Hub, then create a workspace from this
template. Camillia installs the `workspace/` tree as the new workspace's
`.workspace` contract: the agent reads these rules, conventions, camflow bindings,
repository descriptors and docs skeletons before every task. After installation,
adapt the section names, site metadata and pinned versions to your product.

## License

MIT — see [LICENSE](LICENSE).
