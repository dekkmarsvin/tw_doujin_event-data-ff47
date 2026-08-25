# FF47 event data

Sanitized, provenance-tracked data used by [`dekkmarsvin/tw_doujin_event`](https://github.com/dekkmarsvin/tw_doujin_event).

This repository intentionally contains only:

- `event.json`: the versioned event definition, containing organizer roles, category selection, venue-space assignments, and official booth adapter configuration.
- `reference-data-pin.json`: the immutable reference-data commit, per-file hashes, and selected stable IDs.
- `official-booths.json`: booth assignments transcribed from the organizer's published daily lists.
- `map.json`: the repository-authored vector layout published by the code repository's map authoring workflow.
- `PROVENANCE.md`: source and transformation notes.

It does **not** contain the community-maintained workbook, the organizer's floor-plan image, third-party thumbnails, or catalog fields derived from those inputs. There is no blanket license grant over organizer-provided facts or wording; reuse must follow the source-specific provenance and applicable law. The vector layout, schema, validation metadata and documentation are repository-authored artifacts available under the code repository's terms.

Consumers must pin this repository commit and verify file SHA-256 values. They must then fetch and verify `reference-data-pin.json` before resolving `event.json`; neither dependency may follow a floating branch.
