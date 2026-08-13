# MOTM — Meeting of the Minds

A panel of LLM experts answers independently, ranks each other blind, then a
chair adjudicates. By [ALAB](https://github.com/eldaje).

**Live:** https://motm.wtf

## How it works

1. **The panel** — each expert answers the same question alone, with no
   knowledge of the others. Venice is the API door; its own house models are
   excluded from sitting.
2. **Blind peer review** — every expert ranks all the anonymised answers,
   including its own, unlabelled. Results are aggregated by Borda count.
3. **The chair** — chosen *after* the panel reports, not before. Either a
   Venice model in-app, or copy the brief into a Claude conversation.

## Notes

- Single self-contained HTML file. No build step, no dependencies, images
  inlined as data URIs.
- Your Venice API key is stored in `localStorage` on your device only. It is
  never sent anywhere except Venice.
- The passcode is a hashed door, not encryption — the source is public.
- Panel selection takes one model per vendor family and excludes the chair's
  own family. Shared lineage means shared blind spots.

## Lanes

A lane is a framing that rides in front of your question. Straight sends it
untouched. All lanes are editable in settings.
