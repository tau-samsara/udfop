---
title: Demo: Tables
category: Site Guide
summary: Tables with alignment, typed columns, sorting, filtering, a label column and key/value tables.
authors: tau
---

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

## A table

Every table gets a filter box and clickable headings. Click a heading to sort, hold {{Shift}} while clicking to add a second sort, and type in the box to show only matching rows. The words you type are marked in the rows.

| Item | Where it goes | Count |
|:---|:---:|---:|
| Rows | one per line | 12 |
| Cells | separated by pipes | 1,234 |
| Links | [[Controls]] | 7 |

## Column types

A tag in braces after the dashes says what a column holds, so it sorts properly: numbers as numbers, percentages, durations and dates.

| Item | Level | Hit chance | Cooldown | Added |
|:---|---:{num}|---:{pct}|---:{dur}|---{date}|
| Sword | 5 | 85% | 1h 30m | 2026-10-01 |
| Dagger | 12 | 95% | 45m | 2026-09-12 |
| Axe | 30 | 60% | 2h | 2026-10-20 |
| Spear | 9 | 78% | 15m | 2026-08-03 |

## A label column

`{label}` on the first column makes its cells row headings, which keeps each row readable on a phone.

| Skill | Cap | Notes |
|:---{label}|---:{num}|:---|
| Archery | 100 | Needs a bow |
| Block | 100 | Needs a shield |
| Destruction | 200 | Master skill |

## A key/value table

Empty heading cells and `{label}` give a list of facts about one thing, with no heading row and nothing to sort.

| | |
|---{label}|---|
| Region | Hammerfell |
| Level range | 10 to 20 |
| Found in | [[Controls]] |

## A pipe inside a cell

A pipe that belongs in the text is written `\|`:

| Written | Shown |
|---|---|
| `[[Controls\|the key bindings]]` | [[Controls\|the key bindings]] |

## Yes and no

A `{bool}` column sorts `Yes` and `No`, and the ticks and crosses, together.

| Mod | Works offline | Needs restart |
|:---|:---:{bool}|:---:{bool}|
| Audio pack | Yes | No |
| Map fix | No | Yes |
| UI scale | ✓ | ✗ |

## Empty cells sort last

Empty cells and cells holding `-`, `—`, `N/A` or `?` always sort last, whichever way the column is sorted. Click **Level** to see.

| Item | Level |
|:---|---:{num}|
| Sword | 5 |
| Shield | N/A |
| Dagger | 12 |
| Bow | ? |
| Spear | 9 |

## A long table

A table of more than 15 rows shows 15 and scrolls inside its own box, with the heading row staying at the top of the box.

| Level | Renown XP needed | Notes |
|---:{num}|---:{num}|:---|
| 1 | 100 | |
| 2 | 220 | |
| 3 | 360 | |
| 4 | 520 | |
| 5 | 700 | |
| 6 | 900 | |
| 7 | 1,120 | |
| 8 | 1,360 | |
| 9 | 1,620 | |
| 10 | 1,900 | Title unlocked |
| 11 | 2,200 | |
| 12 | 2,520 | |
| 13 | 2,860 | |
| 14 | 3,220 | |
| 15 | 3,600 | |
| 16 | 4,000 | |
| 17 | 4,420 | |
| 18 | 4,860 | |
| 19 | 5,320 | |
| 20 | 5,800 | Cap |

## Copying rows

**Copy MD** and **Copy HTML** above a table copy the rows currently shown, in the order shown. Filter the long table above, then try them: the first gives an aligned table inside a code block (it keeps its lines when pasted into Discord), and the second gives an HTML table that pastes into Excel or Google Sheets as cells.
