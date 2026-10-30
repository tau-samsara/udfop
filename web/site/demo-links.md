---
title: Demo: Links
category: Site Guide
summary: Links to guide pages, Site Guide pages, topics, patches, sections, other websites and pages that do not exist yet.
authors: tau
expected-missing: Example of a missing page
---

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

## Links to other pages

Double square brackets link to another page of this site. A plain name is a Game Guide page, and the marker after the link says where it goes: **GP** for a guide page, **SG** for a Site Guide page, **PN** for Patch Notes and an arrow for another website. The markers are added by the site.

| You type | Result |
|---|---|
| `[[Controls]]` | [[Controls]] |
| `[[Controls\|the key bindings]]` | [[Controls\|the key bindings]] |
| `[[guide:Controls]]` | [[guide:Controls]] |
| `[[site:Fixing a page]]` | [[site:Fixing a page]] |
| `[[topic:Renown]]` | [[topic:Renown]] |
| `[[patch:0.1.8859]]` | [[patch:0.1.8859]] |
| `[[Controls#Mouse]]` | [[Controls#Mouse]] |
| `[[#Other links on this site]]` | [[#Other links on this site]] |
| `[text](https://example.com)` | [an outside link](https://example.com) |
| `[[Example of a missing page]]` | [[Example of a missing page]] |

## Link previews

On a computer, point at a link to a guide page, a topic, a patch or a category to see a short preview of it. Point at any link in the table above.

## Other links on this site

A normal Markdown link can point at any page of the site, starting with `#/`:

| You type | Result |
|---|---|
| `[Player Guide](#/guide/category/Player%20Guide)` | [Player Guide](#/guide/category/Player%20Guide) |
| `[all patches](#/patches)` | [all patches](#/patches) |
| `[recent changes](#/recent)` | [recent changes](#/recent) |
| `[Feedback & Bugs](#/feedback)` | [Feedback & Bugs](#/feedback) |
| `[the glossary](#/glossary)` | [the glossary](#/glossary) |

## A red link

A page that does not exist yet shows a red link, and clicking it starts that page. Listing the name on the `expected-missing:` line of the front matter, as this page does, keeps the page check from warning about a link written on purpose.
