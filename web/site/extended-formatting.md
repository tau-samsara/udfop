---
title: Extended formatting
category: Site Guide
summary: The formatting beyond plain Markdown: links between pages, the References section, picture captions, notice boxes, infoboxes, spoilers, footnotes and keycaps. Each part links to a demo page with examples.
---

> [!INFO]
> Kind: Reference
> Covers: The formatting beyond plain Markdown
> Used on: Game Guide and Site Guide pages
> Written in: Markdown, with a few extras
> ## Related
> Plain Markdown: [[site:Formatting reference]]
> Examples: [[site:Demo: Index]]
> Problems: [[site:Fixing a page]]

These go beyond plain Markdown. They are what lets Game Guide pages connect to each other and to the Patch Notes. Each part has its rule and syntax here and links to a demo page that shows it at work, and [[site:Demo: Index]] lists them all. Plain Markdown is on the [[site:Formatting reference]] page.

### Links to other pages

Double square brackets link to another page on this site, a Patch Notes topic or a patch, so the site knows what you linked and can list it in the References section. Matching is case-insensitive. A plain name always means a Game Guide page: the site never guesses that you meant a Site Guide page or a topic. A bar followed by your own words changes the text that is shown.

| You type | It links to |
|---|---|
| `[[Controls]]` | a Game Guide page by its title (`guide:` before the title says so out loud, and means the same) |
| `[[Controls\|the key bindings]]` | the same page, with your own words |
| `[[site:Fixing a page]]` | a Site Guide page |
| `[[topic:Revenants]]` | a Patch Notes topic |
| `[[patch:0.1.6656]]` | a patch |
| `[[Controls#Mouse]]` | a section of a guide page |
| `[[#Link markers]]` | a section of the page you are writing |
| `[text](https://example.com)` | another website |

A page that does not exist yet shows as a **red** link, and clicking it starts that page, so you can plan a set of pages by linking first. A red link you write on purpose can be listed on an `expected-missing:` line of the front matter, so the page check stays quiet.

**Linking to a section.** Put a `#` and the words of a heading after the page name. Capitals and punctuation do not matter, and the heading must be one of the first three levels. Sections work for guide pages and Site Guide pages only, not for topics or patches. For a section of a topic, use a plain link such as `[History](#/topic/Resting#s-history)`. The page check tells you when a page has no such section.

**Other pages of the site.** A normal Markdown link starting with `#/` can point at a category, a Patch Notes list or the feedback page, such as `[all patches](#/patches)`. These are plain links: they have no marker and do not appear in the References section.

The [[site:Demo: Links]] page shows each form, and more cases.

### Link markers

A small raised marker after a link says where it goes, so readers know before they click. The markers are added for you, so do not type them.

| Marker | Where the link goes |
|---|---|
| **GP** | a page in the Game Guide |
| **SG** | a page in the Site Guide |
| **PN** | a Patch Notes topic or patch |
| **↗** | another website |
| none | a plain link to a page of this site, and a red link to a page that does not exist yet |

On a computer, pointing at a link to a guide page, a topic, a patch or a category also shows a short preview of it. Nothing is written for this, and readers can turn previews off in the settings panel.

### The References section

Every guide page that links anywhere gets a **References** section at the bottom. Do not write it yourself: the site builds it from the links in your text, listing each link once, in the order it first appears.

| Part | What it lists |
|---|---|
| **Game Guide** | the guide pages you linked, each with its summary |
| **Site Guide** | the Site Guide pages you linked |
| **Patch Notes** | the topics and patches you linked, each with when it was last changed |
| **External Links** | the outside websites you linked |

**`related:` (optional).** To list a page, topic or patch that does not belong in a sentence, add a `related:` line to the front matter, with names separated by commas. A name with no prefix is a Game Guide page, as in the text. Start a name with `site:`, `topic:` or `patch:` for the other kinds (`guide:` is also allowed). The page check warns about names that match nothing.

```md
related: guide:Party rest, site:Formatting reference, topic:Resting, patch:0.1.6656
```

The [[site:Demo: References]] page shows the section built from links and a `related:` line.

### Picture captions and placement

To caption a picture or move it to the side, put the caption in quotes after the path, and a side and width in braces after the picture. Both parts are optional. A caption, a side or a width only works when the picture is **alone on its line**.

| You type | You get |
|---|---|
| `![alt](images/x.png "Caption")` | a framed picture on the **right**, 240 pixels wide, with the caption under it |
| `![alt](images/x.png "Caption"){left 180}` | the same, floated to the left and 180 pixels wide |
| `![alt](images/x.png "Caption"){center 400}` | centered on its own line, 400 pixels wide |
| `![alt](images/x.png){right 200}` | a floated picture with no caption |
| `![alt](images/x.png)` | the plain picture |

The side is `left`, `right` or `center`, and the width is a number of pixels from 40 to 1200. The picture never grows past its own size or past the page. Text wraps around a floated picture, and a heading, table or centered picture starts below it. On a phone the picture moves above the text. Write the caption as a short sentence naming what is shown, and keep the alt text for describing what it looks like. The page check warns about any other word in the braces.

The [[site:Demo: Pictures]] page shows each placement.

### Notice boxes

A notice box sets a tip, a warning or an extra fact apart from the text around it. Start a quotation with a tag on a line of its own, then write the box on the lines after it. The tag is not case sensitive.

```markdown
> [!WARNING]
> Quicksaving during a quest can break it.
```

| You write | The box is labelled | Use it for |
|:---|:---|:---|
| `[!NOTE]` | Note | extra information |
| `[!TIP]` | Tip | helpful advice |
| `[!IMPORTANT]` | Important | something readers must know |
| `[!WARNING]` | Warning | something that can go wrong |
| `[!CAUTION]` | Caution | something that can lose progress or data |

Anything you can write in a page also works inside a box, with `>` at the start of every line, including blank lines between paragraphs. Keep each box short and use them sparingly, since a page full of boxes stops anything standing out. A tag the site does not know, such as `[!DANGER]`, leaves an ordinary quotation, and the page check mentions it.

The [[site:Demo: Notice boxes]] page shows all five and what a box can hold.

### Infoboxes

An infobox is a small panel of key facts that floats beside the first paragraphs of a page, so readers see the numbers they look up most, such as a price or a weight, at a glance. Start a quotation with `[!INFO]` and an optional title, then write one fact per line as `Key: value`.

```markdown
> [!INFO] Example item
> image: images/sarsaparilla-01s.jpg
> Type: Example
> Value: 100 gold
> ## Where found
> Sold at: General Stores
```

- **Title.** Written after `[!INFO]`. Leave it out and the page's own title is used.
- **Rows.** Each `Key: value` line is one row. The value can hold bold text and links. A line with no colon carries on the row above it.
- **Picture.** An optional `image:` line, with the path from the page's folder, puts a picture under the title.
- **Group headings.** A line starting `## ` adds a gray heading that splits the rows into groups. It is not a section of the page.
- **Placement.** Put the infobox first, right after the front matter, so it lines up with the top of the page text. It floats on the right, and moves above the text on a phone.

Use one infobox per page and keep it to the facts a reader looks up. The page check notes a row with no value, a page with more than one panel, and a panel that is not first. In GitHub's preview the panel shows as an ordinary quotation.

The [[site:Demo: Infobox]] page shows a panel at work.

### Spoilers

To hide a few words until the reader chooses to see them, put `>!` before them and `!<` after them.

```markdown
The final boss is >!the Lich King, who is weak to fire!<, so bring fire spells.
```

The words are masked by a dark bar. Clicking them, or pressing {{Enter}} or {{Space}} while they are selected, shows them, and the same action hides them again. Bold, italic, links and keys work inside a spoiler.

A spoiler hides words from the eye, not from the page: the text is still in the file on GitHub and can be selected and copied. Use it for surprises in the game, never for anything private. A spoiler must sit on one line, and a line that starts with `>!` is a paragraph, not a quotation.

The [[site:Demo: Spoilers]] page shows more cases.

### Footnotes

To name the source of a statement without cluttering the sentence, put `[^name]` after it and write the note on a line of its own, anywhere on the page.

```markdown
Writs can award Renown XP.[^writs]

[^writs]: https://example.com/source
```

The reference becomes a small numbered link, and the notes are listed under a **Footnotes** heading at the end of the page, before References.

- **Numbering** follows the order the references first appear in the text. Using the same name again reuses its number, and the note gets a way back for each use.
- **A note** can hold links, bold and italic. A note that is only an address shows it as a link. A long note can continue on indented lines after it.
- **Names** are letters, digits, hyphens and underscores. They are never shown, only the numbers.
- **The page check** reports a reference with no note (it is shown as written), a name defined twice, and a note that is never used (it is not shown). In the editor, **Format > Snippets > Footnote** adds a reference at the caret and its note at the end of the page.

A note cannot hold another footnote, and a note inside a quote or a notice box is not recognized: write it on a line of its own, at the left edge.

The [[site:Demo: Footnotes]] page shows more cases.

### Keys and buttons

To show a keyboard key, a mouse button or a gamepad button, put its name between double braces. It is drawn as a small keycap. Use keycaps for things you **press**, and bold for buttons and menu labels you **click on screen**, such as **Rest**, so the two are never mixed up.

```md
Press {{W}} to move forward and hold {{Left Shift}} to run.
{{Shift+Right click}} draws the bow, and {{Mouse 4}} switches the view.
On a controller, hold {{pad:RT}}.
```

- **Arrow keys** are typed as words (`{{Up}}`, `{{Down}}`, `{{Left}}`, `{{Right}}`) and shown as arrows. The words are only for the four arrow keys.
- **Combinations** are joined with `+`, and each key gets its own cap, as in `{{Ctrl+Shift+K}}`. For a plus key itself, write `{{+}}`.
- **Mouse buttons** are recognized by name (`Left click`, `Right click`, `Middle click`, `Mouse 3`, `Mouse 4`, `Mouse 5` and `Scroll`) and drawn with rounder corners.
- **Gamepad buttons** start with `pad:`, as in `{{pad:A}}`, and are drawn round. The prefix is not shown. When a page gives both controllers for one button, put the Xbox name first and the PlayStation name second, such as `{{pad:RB}}, {{pad:R1}}`, and say so once on the page.
- **Keys with symbols** are written as the character and named in plain words after it: `{{;}} (semicolon)`, `{{,}} (comma)`.
- **Use the same names everywhere** so pages agree. Use these:

| Kind | Names |
|---|---|
| Letters and digits | `A` to `Z` and `0` to `9`, as the character |
| Function and editing | `F1` to `F12`, `Esc`, `Tab`, `Enter`, `Space`, `Backspace`, `Insert`, `Delete`, `Home`, `End`, `PgUp`, `PgDn` |
| Arrows | `Up`, `Down`, `Left`, `Right` (shown as ↑ ↓ ← →) |
| Modifiers | `Shift`, `Left Shift`, `Right Shift`, `Ctrl`, `Alt`, and `Left` or `Right` in front of each |
| Gamepad (Xbox) | `A`, `B`, `X`, `Y`, `LB`, `RB`, `LT`, `RT`, `LSB` (left stick button), `RSB` (right stick button), `D-pad`, `D-pad Up`, `D-pad Down`, `D-pad Left`, `D-pad Right`, `Start`, `Back` |
| Gamepad (PlayStation) | `Cross`, `Circle`, `Square`, `Triangle`, `L1`, `R1`, `L2`, `R2`, `L3`, `R3`, `D-pad`, `Start`, `Select` |
| Number pad | `Numpad 0` to `Numpad 9`, `Numpad +`, `Numpad -`, `Numpad *`, `Numpad /`, `Numpad Enter` |

Keycaps work in tables and in captions, but not inside the text of a link. Put an example in single backticks when you want to show the braces themselves.

The [[site:Demo: Keys and buttons]] page shows each kind.

### What the site does for you

You do not write these. They come from what you wrote: a **Contents** list built from the page's headings (docked in the left sidebar by default, where it follows the section being read; subsections are listed under their section behind a small arrow that the reader opens; readers can hide it behind a ☰ button beside the page title that floats at the top left of the window once they scroll past the title, and the site remembers their choice; on a narrow screen such as a phone there is no Contents list: each section and subsection folds instead, closed to begin with, and a reader taps a heading to open it), the page's place in the Game Guide index and breadcrumb from its `category`, its entry in the Game Guide index and in search, the **References** section, the **PN** and **↗** markers on links, and the colors and **Copy** button on code boxes.

## Not supported

Raw HTML (it is shown as plain text, which keeps pages safe and consistent), strikethrough, underline, colored text, task-list checkboxes, merged table cells, embedded video or other media, forced line breaks inside a paragraph, and links to a section of a Patch Notes topic or patch (sections of guide pages and Site Guide pages can be linked, as shown under Links to other pages). Leave these out and the page will look right everywhere.

Back to the [Site Guide](#/site).
