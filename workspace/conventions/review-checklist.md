# Docs review checklist

The reviewer — human or the docs-review camflow — verifies:

- [ ] `uv run mkdocs build --strict` passes with zero warnings (no broken links).
- [ ] Each page sits in the right Diataxis section and is added to `nav:`.
- [ ] Style rules hold: second person, present tense, runnable samples.
- [ ] New commands were actually executed against a current environment.
- [ ] Placeholders use `<angle-brackets>` and are explained on first use.
- [ ] Images have alt text and are compressed.
- [ ] Front matter carries a `description:`.
- [ ] Cross-links from related pages were added.
