# Components of the docs product

| Component | Where | Responsibility |
| --- | --- | --- |
| Content | `docs/docs/` | The documentation itself (Markdown). |
| Site configuration | `docs/mkdocs.yml` | Navigation, theme, plugins. |
| Build pipeline | CI | `mkdocs build --strict` gate plus per-PR previews. |
| Version publisher | CI (mike) | Publishes per-release versions to the hosting branch. |
| Hosting | static hosting behind the product domain | Serves the built site. |

The docs site is static: there is no server-side component, no database and no
user data of any kind.
