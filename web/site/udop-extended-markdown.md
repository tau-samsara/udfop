---
title: UDOP Extended Markdown
category: Site Guide
summary: A short course in UDOP Extended Markdown: the Markdown a guide page is written in, the way this site reads it, from the first line of the file to tables, links and the site's own extras.
authors: tau
---

> [!INFO]
> Kind: Tutorial
> Covers: Writing Markdown for a guide page
> Time: About 20 minutes
> Used on: Game Guide and Site Guide pages
> ## Related
> Every rule: [[site:Formatting reference]]
> The extras: [[site:Extended formatting]]
> Examples: [[site:Demo: Index]]
> Practice: [[site:How to use the editor]]

Markdown is plain text with a few marks that tell a program how to lay it out: a `#` for a heading, `**` for bold, `-` for a list. A guide page is a Markdown file, and this site turns it into the page readers see. The Markdown a guide page is written in is called **UDOP Extended Markdown**: ordinary Markdown, read the way this site reads it, plus a few extras that belong to this site, such as links between pages, notice boxes, keycaps and footnotes. This course teaches the marks in the order you need them, and points out where UDOP Extended Markdown differs from the Markdown you may know. Every lesson has a demo page with the full set of examples, so keep this page open beside the editor and try each one.

> [!TIP]
> The quickest way to learn is to type each example into the [[site:How to use the editor|editor]] and watch the preview beside it. The **Problems** button tells you straight away when something is off.

## Lesson 1: The parts of a page file

A page file has two parts. The **front matter** is a few lines at the top between two lines of three dashes, and the **body** is everything under it.

```markdown
---
title: Healing potions
category: Items
summary: What each potion heals and where to buy it.
authors: your name
---

The body starts here, with an opening paragraph.

## A section
```

| Line | What it is |
|---|---|
| `title` | The page's name. It must not match another page, and it is what other pages link to. |
| `category` | The group the page is listed under. Reuse one that exists. |
| `summary` | One sentence, shown in lists, search and hover previews. |
| `authors` | Who wrote the page, separated by commas. |

Do not repeat the title as a `#` heading: the site shows it for you. More lines, such as `related`, are in [[site:Demo: Front matter]].

## Lesson 2: Paragraphs and headings

A **blank line** starts a new paragraph. A single line break inside a paragraph is only a space, so these three lines are one paragraph:

```markdown
Resting restores health
and Magicka over time,
but only away from enemies.
```

A heading is `##` and a **space** and the words. Start at `##`, use `###` for a sub-section, and leave the space: `##Rest` is shown as plain text, and the page check says so.

```markdown
## Resting

### In a dungeon
```

- `##` and `###` headings are what the **Contents** list is built from. On a phone they fold shut, so keep each one short and clear.
- Headings deeper than `###` are shown but are not in the Contents.
- A section's address is made from its words, so `[[#In a dungeon]]` links to it.

See [[site:Demo: Headings]].

## Lesson 3: Emphasis and code

| You type | You get |
|---|---|
| `**bold**` | **bold**, for names and labels |
| `*italic*` or `_italic_` | *italic*, for emphasis |
| `` `Jump` `` | `Jump`, for text exactly as typed |

Only `**` makes bold, and `~~strikethrough~~` and underline are not supported. Backticks also keep marks from being read, so `` `[[a page]]` `` shows the brackets instead of making a link. See [[site:Demo: Text]].

## Lesson 4: Lists

Start a line with `- ` for a bullet or `1. ` for a number, and indent a line two spaces to nest it.

```markdown
- Potions
  - Healing
  - Magicka
1. Open the map
2. Pick a town
```

Numbers are renumbered for you, so a list written `1.` `1.` `1.` still reads 1, 2, 3. A list can follow a paragraph on the next line without a blank line. See [[site:Demo: Lists]].

## Lesson 5: Links

The site has three kinds of link, and the **double brackets** are the ones to learn.

| You type | It links to |
|---|---|
| `[the wiki](https://example.com)` | another website |
| `[[Controls]]` | a Game Guide page, by its title |
| `[[Controls\|the key bindings]]` | the same page, with your own words |
| `[[Controls#Mouse]]` | one section of that page |
| `[[site:Fixing a page]]` | a Site Guide page |
| `[[topic:Renown]]` | a Patch Notes topic |
| `[[patch:0.1.8859]]` | a patch |

- A plain name is **always** a Game Guide page. The site never guesses, so a Site Guide page, a topic or a patch needs `site:`, `topic:` or `patch:` in front.
- Capitals do not matter, but the words do. A page that does not exist shows a **red** link, and clicking it starts that page.
- The site adds a small marker after each link and builds a **References** section at the bottom from your links, so do not write one.

See [[site:Demo: Links]] and [[site:Demo: References]].

## Lesson 6: Pictures

A picture is a link with an exclamation mark in front: the words that describe it in square brackets, then the path to the file in round brackets, as in `![what it shows](images/name.png)`. A picture **alone on its line** can have a caption and a side:

```markdown
![A Redguard town](images/town.png "Sentinel at dusk."){right 240}
```

The side is `left`, `right` or `center`, and the width is in pixels. See [[site:Demo: Pictures]].

## Lesson 7: Quotes and notice boxes

A line starting with `>` is a quotation. If its first line is a tag in brackets, it becomes a box instead:

```markdown
> [!WARNING]
> Resting in a dungeon can wake monsters.
```

The tags are `NOTE`, `TIP`, `IMPORTANT`, `WARNING` and `CAUTION`, and every line of the box starts with `>`. Keep boxes short and rare, or none of them stands out. `> [!INFO]` is different: it is the fact panel on the right of the page. See [[site:Demo: Notice boxes]], [[site:Demo: Quotes]] and [[site:Demo: Infobox]].

## Lesson 8: Code boxes

Three backticks above and below make a box with a **Copy** button. A language name after the opening backticks adds colors:

````markdown
```json
{ "volume": 80 }
```
````

The box keeps spaces and line breaks exactly, so use it for commands, settings and chat lines. See [[site:Demo: Code blocks]] for the languages.

## Lesson 9: Tables

A header row, a divider row of dashes, then one row per line, with `|` between the cells.

```markdown
| Potion | Heals | Price |
|:---|---:|---:|
| Minor | 20 | 50 |
| Major | 80 | 200 |
```

- Colons in the divider set the alignment: `:---` left, `:---:` center, `---:` right.
- Every table can be sorted, filtered and copied by the reader, with nothing extra from you. Add a tag such as `{num}` to the divider (`---:{num}`) to sort a column of numbers as numbers.
- A `|` inside a cell is written `\|`.
- A table needs its header row and its divider row, and every row should have the same number of cells.

See [[site:Demo: Tables]].

## Lesson 10: The site's extras

Three small extras are worth knowing early:

| You type | You get |
|---|---|
| `>!the answer!<` | words hidden until the reader clicks them |
| `{{W}}` and `{{Shift+Right click}}` | a keycap for a key or a button |
| `text[^1]` with `[^1]: the source` | a numbered footnote |

See [[site:Demo: Spoilers]], [[site:Demo: Keys and buttons]] and [[site:Demo: Footnotes]].

## Where this site differs from other Markdown

Other sites read some marks differently, so watch for these:

- **Raw HTML is shown as plain text.** Tags such as `<b>` or `<br>` do nothing, and the page check mentions them.
- **There are no forced line breaks** inside a paragraph, and no strikethrough, underline, colored text, checkboxes, merged table cells or embedded video.
- **A backslash does not escape a mark** outside a table. To show a `*` or a bracket as it is, put it in backticks.
- **A quote with a tag is a box.** An unknown tag such as `[!DANGER]` stays a plain quote.
- **A link to a section** works for guide and Site Guide pages, not for topics or patches.

The full list is under **Not supported** on [[site:Extended formatting]].

## Check your page

Before you send a page, run through this:

1. The front matter has a `title`, `category`, `summary` and `authors`, and the title is not repeated as a heading.
2. Every heading has a space after its hashes, and the first is `##`.
3. Every code box that was opened is closed.
4. Every `[[link]]` goes where you meant, and any red link is on purpose.
5. The **Problems** button in the editor is green.

If it is not, [[site:Fixing a page]] explains each message.

## Where to go next

- [[site:Formatting reference]] has every rule of plain Markdown.
- [[site:Extended formatting]] has the site's own extras.
- [[site:Demo: Index]] has one example page for each feature.
- [[site:How to write a guide page]] walks through sending your page, from the first fork to seeing it live.

Back to the [Site Guide](#/site).
