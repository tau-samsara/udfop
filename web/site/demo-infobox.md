---
title: Demo: Infobox
category: Site Guide
summary: An infobox, the panel of key facts that floats beside the first paragraphs of a page.
authors: tau
---

> [!INFO] Example item
> image: ../placeholder.svg
> Type: Example
> Value: 100 gold
> Weight: 2 kg
> ## Where found
> Sold at: General Stores
> Seen in: [[Controls]]

An infobox floats on the right and lines up with the top of the page text. It is a small panel of the facts a reader looks up most, such as a price or a weight, so they do not have to read the page for them.

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

Each `Key: value` line is a row, and a value can hold **bold** text and links. A line starting with `##` adds a gray group heading, as **Where found** does here.

## The text carries on beside it

The headings, notice boxes and tables of the page sit beside the panel too. On a phone it moves above the text.

> [!NOTE]
> Use one infobox per page, as the first thing on the page. The page check warns about a row with no value, a second panel, and a panel that is not first.

A table starts below the panel, never beside it, so it keeps its width:

| Item | Value |
|---|---|
| Sword | 100 |
| Axe | 120 |
