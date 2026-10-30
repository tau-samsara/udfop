---
title: Formatting reference
category: Site Guide
summary: The plain Markdown a guide page can use, with the syntax to type. Each part links to a demo page with examples. The site's own extras are on Extended formatting.
---

> [!INFO]
> Kind: Reference
> Covers: The plain Markdown a guide page can use
> Used on: Game Guide and Site Guide pages
> Written in: Markdown, with a few extras
> ## Related
> Extras: [[site:Extended formatting]]
> Examples: [[site:Demo: Index]]
> Course: [[site:UDOP Extended Markdown]]
> Steps: [[site:How to write a guide page]]
> Problems: [[site:Fixing a page]]

The plain Markdown you can write in a guide page: the rule and the syntax for each part. Every part links to a demo page that shows it at work, and [[site:Demo: Index]] lists them all. The extras that are particular to this site, such as links between pages, notice boxes and keycaps, are on [[site:Extended formatting]]. For the steps of adding or editing a page, see [[site:How to write a guide page]]. If something does not look right, see [[site:Fixing a page]].

## Quick reference

| You type | You get | Details under |
|---|---|---|
| `## Heading` | a section heading (`###` for a sub-section) | Headings |
| `**bold**` and `*italic*` | **bold** and *italic* | Bold and italic |
| `- item` or `1. item` | a bullet or a numbered list | Lists |
| `> words` | a quotation | Quotations |
| `---` | a divider | Horizontal divider |
| `` `inline code` `` | `inline code` | Inline code |
| three backticks, then a language name `` ```[language] `` | a code box with a Copy button | Code blocks |
| `[words](https://example.com)` | a link to another website | Links to other websites |
| `[[Page title]]` | a link to a guide page | [[site:Extended formatting#Links to other pages]] |
| `[[topic:Name]]` and `[[patch:0.1.6656]]` | a link to a Patch Notes topic or patch | [[site:Extended formatting#Links to other pages]] |
| `![alt](images/x.png "Caption"){right 220}` | a picture, with a caption, on one side | [[site:Extended formatting#Picture captions and placement]] |
| `> [!NOTE]` then the text on the next line | a notice box | [[site:Extended formatting#Notice boxes]] |
| `> [!INFO]` then `Key: value` lines | a fact panel beside the text | [[site:Extended formatting#Infoboxes]] |
| `>!hidden words!<` | words hidden until clicked | [[site:Extended formatting#Spoilers]] |
| `{{W}}` and `{{Shift+Right click}}` | keycaps | [[site:Extended formatting#Keys and buttons]] |
| `text[^name]` and `[^name]: note` | a numbered footnote | [[site:Extended formatting#Footnotes]] |

## Basic formatting

These are plain Markdown, the same on any site that uses it.

### Paragraphs

A blank line starts a new paragraph. A single line break inside a paragraph is only a space, so to put something on its own line, make it its own paragraph or use a list.

### Headings

Start a line with `##` and a space for a section heading, `###` for a sub-section, and `####` to `######` for deeper levels. The page title is added for you, so start at `##`. The first three levels build the **Contents** list.

```md
## A section
### A smaller section
```

The [[site:Demo: Headings]] page shows more cases.

### Bold and italic

Put `**` around text for bold, and `*` or `_` around it for italic.

```markdown
This is **bold**, this is *italic*, and this is _also italic_.
```

The [[site:Demo: Text]] page shows more cases.

### Lists

Start lines with `- ` or `* ` for bullets and `1. ` for numbers. Indent a line two spaces more than the item above it to nest it one level deeper. A list reads best with no more than three levels.

```md
- A bullet
  - A nested bullet
1. A numbered step
```

The [[site:Demo: Lists]] page shows more cases.

### Quotations

Start a line with `>` for a quotation, which suits in-game text or developer statements. Say who said it and where it came from in a line under the quotation, with a `>` on the blank line between the two, and add a link when there is one.

```md
> Quotations are set off from the text.
>
> Who said it, and where it came from
```

A quotation whose first line is a tag such as `[!NOTE]` becomes a notice box instead. See [[site:Extended formatting#Notice boxes]].

The [[site:Demo: Quotes]] page shows more cases.

### Horizontal divider

Three dashes on a line of their own draw a divider.

```md
---
```

### Inline code

Put a short stretch between single backticks to show it exactly as typed. This is also how to show markup literally, so it is not turned into a link or bold. To show a backtick, open and close the code with more backticks than it contains and leave a space inside each end.

```md
Press `Jump` to climb, and write `[[a page]]` to link.
Write `` `word` `` to show word in backticks.
```

The [[site:Demo: Text]] page shows more cases.

### Code blocks

For several lines shown exactly as typed, put a line of three backticks above them and another below. Spacing and line breaks are kept, long lines scroll sideways, and every box has a **Copy** button in its top bar.

(Optional) Put a language name straight after the opening backticks, for example `json`. The name appears in the box's top bar and the code is colored. A box with no name, or with a name the site does not know, is shown plain, and a name you gave still appears in the bar. Names are not case sensitive.

| You write | The code is colored as |
|:---|:---|
| `json` | JSON |
| `js`, `javascript`, `ts`, `typescript` | JavaScript and TypeScript |
| `bash`, `sh`, `zsh`, `shell`, `console` | Shell commands (a leading `$` or `>` prompt is picked out) |
| `powershell`, `ps1`, `pwsh` | PowerShell |
| `bat`, `batch`, `cmd` | Windows batch files |
| `ini`, `conf`, `cfg`, `config`, `toml`, `properties` | Settings files |
| `yaml`, `yml` | YAML |
| `lua` | Lua |
| `cs`, `csharp`, `c#` | C# |
| `xml`, `html`, `xaml`, `svg` | XML and HTML |
| `python`, `py` | Python |
| `markdown`, `md` | Markdown, including `[[links]]` and `{{keys}}` |
| `text`, `txt`, or no name | no colors |

The coloring is a guide for the eye, not a full reader of the language, and the text itself is never changed. Very long boxes (over about 20,000 characters) are shown without colors.

A box ends only at a line of backticks at least as long as the one that opened it, so to show a box that contains three backticks, open and close it with four. Tildes, written `~~~`, work as fences too.

````md
```bash
echo "a box inside a box"
```
````

The [[site:Demo: Code blocks]] page shows each language and more cases.

### Links to other websites

Write the words in square brackets and the address in round brackets.

```md
[a link to GitHub](https://github.com)
```

### Tables

A header row, a line of three dashes per column under it, then one row per line, with `|` between the cells. Cells can hold bold text, links and code. Colons in the line of dashes set each column's alignment: `:---` left (the default), `:---:` centered, `---:` right, which suits numbers. A `|` that belongs inside a cell is written `\|`.

```md
| Item | Where it goes | Count |
|:---|:---:|---:|
| Rows | one per line | 12 |
```

Readers can sort a table by clicking a heading, filter it by typing, and copy the rows shown with **Copy MD** and **Copy HTML**. These controls are added to every table, so nothing is needed in the Markdown. A table of more than 15 rows scrolls inside its own box.

To say what a column holds, put a **type tag** in braces at the end of its cell in the line of dashes, after the alignment colons, so it sorts properly. A column with no tag is read as the first type that fits all of its cells.

| Tag | The column holds | For example |
|---|---|---|
| `{num}` | numbers | `1,200`, `-3`, `1.5k` |
| `{pct}` | percentages | `85%` |
| `{dur}` | durations | `1h 30m`, `45s`, `2:30` |
| `{date}` | dates | `2026-10-24`, `Oct 24, 2026` |
| `{bool}` | yes or no | `Yes`/`No`, `✓`/`✗` |
| `{text}` | text | anything |
| `{label}` | the first column's cells are row headings | |

```md
| Item | Level | Cooldown |
|:---|---:{num}|---:{dur}|
| Sword | 5 | 1h 30m |
```

For a list of facts about one thing, use a **key/value table**: leave the heading cells empty and put `{label}` on the first column. It has no heading row and nothing to sort or filter.

```md
| | |
|---{label}|---|
| Region | Hammerfell |
```

In the editor, **Format > Table Column** sets the tag for the column the cursor is in, and **Format > Snippets > Key/Value Table** starts a key/value table.

The [[site:Demo: Tables]] page shows each of these, and more cases.

### Pictures

An exclamation mark, the description in square brackets, and the picture's path in round brackets. How to add the picture file itself is explained in [[site:How to write a guide page|the how-to]], under **Adding pictures**.

```md
![A description of the picture](images/name.png)
```

Readers can click any picture to open it and zoom in. If a picture's file cannot be found, readers see a gray "No picture yet" box in its place, and the page check reports the missing file as an error. Captions and placement are on [[site:Extended formatting#Picture captions and placement]].

The [[site:Demo: Pictures]] page shows more cases.

## Going further

Links between pages, the References section, picture captions and placement, notice boxes, infoboxes, spoilers, footnotes and keycaps are on [[site:Extended formatting]], which also lists what is not supported. For what the site builds around your text, see [[site:Anatomy of a page]].

Back to the [Site Guide](#/site).
