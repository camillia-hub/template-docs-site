# Content structure rules

- The information architecture follows Diataxis: every page is exactly one of
  tutorial, how-to guide, reference or explanation, and lives in the matching
  section (`tutorials/`, `how-to/`, `reference/`, `explanation/`).
- A page starts with a one-sentence purpose; reference pages use tables for
  options and flags.
- Every page carries a `description:` in its front matter (used for search and
  link previews).
- New pages are added to the `nav:` in `mkdocs.yml` in the same commit; orphan
  pages fail review.
- Internal links are relative and point at the target file
  (`../how-to/deploy.md`), never at rendered URLs — the strict build catches
  broken links.
- Generated reference pages (CLI, API) are never hand-edited; fix the source and
  regenerate.
