# Provenance

## `event.json`

- Event: Fancy Frontier 47
- Organizer event page: <https://www.f-2.com.tw/ff47%E4%B8%89%E6%97%A5%E6%94%A4%E4%BD%8D%E7%B7%A8%E8%99%9F%E5%85%AC%E4%BD%88/>
- Repository-authored fields: schema version, adapter identifier, normalized timestamps, area identifiers, organizer roles, category selection, and venue-space assignments.
- Organizer, category catalog, venue, and venue-space facts are resolved only from the immutable commit and per-file hashes in `reference-data-pin.json`.

## `reference-data-pin.json`

- Organizer and category source: <https://www.f-2.com.tw/> and <https://www.f-2.com.tw/%E7%A4%BE%E5%9C%98%E4%B8%BB%E9%A1%8C%E9%A1%9E%E5%88%A5/>
- Venue source: <https://www.expopark.taipei/FieldInfo_Detail.aspx?n=205&s=1>
- The pin selects the reviewed `frontier-anime` organizer, its immutable `circle-topics@2026-08-25` catalog, `taipei-expo-park-zhengyan-hall`, and `zhengyan-exhibition-area`.
- The selected reference commit and every consumed JSON file are fixed by SHA; missing or mismatched data must fail closed.

## `official-booths.json`

- Day 1: <https://www.f-2.com.tw/%E3%80%90ff47%E3%80%91%E7%AC%AC%E4%B8%80%E5%A4%A9%E6%94%A4%E4%BD%8D%E7%B7%A8%E8%99%9F/>
- Day 2: <https://www.f-2.com.tw/%E3%80%90ff47%E3%80%91%E7%AC%AC%E4%BA%8C%E5%A4%A9%E6%94%A4%E4%BD%8D%E7%B7%A8%E8%99%9F/>
- Day 3: <https://www.f-2.com.tw/%E3%80%90ff47%E3%80%91%E7%AC%AC%E4%B8%89%E5%A4%A9%E6%94%A4%E4%BD%8D%E7%B7%A8%E8%99%9F/>
- Transformation: HTML table rows normalized to `{ day, code, name }`, with source URL and fetch metadata retained. Parsing fails closed on missing tables, non-200 responses and implausible row counts.

No community workbook fields are merged into this file.

## `map.json`

- Source artifact: the vector layout previously published by `dekkmarsvin/tw_doujin_event`.
- Transformation: the site's authoring workflow records normalized booth rectangles, structural landmarks and accessibility labels; the organizer's original floor-plan image is not embedded or redistributed.
- Validation: the layout is accepted only after the event-specific row, slot, pillar and access-point checks pass.
