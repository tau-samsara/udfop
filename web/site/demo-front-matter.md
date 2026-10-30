---
title: Demo: Front matter
category: Site Guide
summary: The lines at the top of a page: title, category, summary, authors, related, unlisted and expected-missing.
authors: [tau](https://github.com/tau-samsara), A Contributor Without Git
related: guide:Controls, site:How to use the editor, topic:Renown
expected-missing: Not written yet
---

## The lines at the top

The block between the two `---` lines at the top of this page is its front matter. Each line is `name: value`.

| Line | What it does | Required |
|---|---|---|
| `title` | The page's name, shown as its heading and used in `[[links]]`. It must be unique across both guides. | Yes |
| `category` | The group the page is listed under on the Game Guide front page. | Yes |
| `summary` | One sentence for hover previews, lists and search. | Yes |
| `authors` | The people to credit under the title, separated by commas. `[name](link)` makes a name a link. | No, but the page check warns when it is missing |
| `related` | Pages, topics and patches to list in the References section without linking them in the text. | No |
| `unlisted` | `true` keeps the page out of the lists and categories (see [[site:Demo: Unlisted page]]). | No |
| `expected-missing` | Page names you link on purpose before the page exists, so the page check stays quiet. | No |

## What this page shows

- **Under the title**, a line reads "Written by", with the first author as a link and the second as plain text.
- **A created and updated line** follows it, taken from the page's history once it is committed.
- **At the bottom**, the References section lists the three `related:` entries.
- **A red link** to [[Not written yet]] shows in red, with no warning, because it is listed under `expected-missing:`.

> [!TIP]
> Open the **View Source** tab of this page to see the lines as written.
