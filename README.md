# Angloform Wiki

Angloform Wiki is a translation of a few important Wikipedia articles into
[Angloform](https://github.com/kantord/minglish) — a restricted, unambiguous
subset of English with a real LALR(1) grammar.

Every sentence in every article here parses in the Angloform grammar (see
the parent project's `just lint-file` tool). Translations are adaptations,
not machine output: sentences are rewritten, split, and simplified to fit
the language's grammar while preserving the source's meaning.

## Layout

- `articles/` — one file per translated article. Each file opens with a
  source/attribution block (see below) before the translated text.
- `LICENSE` — the license for all article text (CC BY-SA 4.0, same as
  Wikipedia).
- `ATTRIBUTION.md` — attribution policy and the index of every source
  article translated here.

## Attribution and license

Wikipedia's text is licensed CC BY-SA 4.0 (dual-licensed with the GFDL).
A translation is a derivative work, so every article file here:

1. names the source article and the exact revision translated,
2. states plainly that it is a translation, not endorsed by the original
   authors, and
3. is itself released under CC BY-SA 4.0 — the same license, as required.

See `ATTRIBUTION.md` for the full policy and the per-article source index.

## Adding an article

1. Pick a Wikipedia article and note its permanent revision link
   (`Page information` → `Permanent link`, or `?oldid=<id>`).
2. Translate the text into Angloform, sentence by sentence — see the
   parent repo's `skills/angloform/SKILL.md` for the grammar.
3. Validate every sentence: `just lint "<sentence>"` from the parent repo,
   or `just lint-file wiki/articles/<name>.md`.
4. Add the article's attribution block (copy the template in
   `ATTRIBUTION.md`) and an entry in `ATTRIBUTION.md`'s index.
