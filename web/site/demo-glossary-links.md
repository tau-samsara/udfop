---
title: Demo: Glossary links
category: Site Guide
summary: Linking a page's terms to the glossary, in the two forms that work.
authors: tau
---

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

## In a sentence

A character earns [Renown](#/glossary#gl-renown) online. The same term can be linked through the Glossary guide page, where each term is a heading: [[Glossary#Renown]], or with your own words, [[Glossary#Renown|Renown level]].

## What was written and what it gives

| Written | Result | Goes to |
|---|---|---|
| `[Renown](#/glossary#gl-renown)` | [Renown](#/glossary#gl-renown) | The entry on the glossary page |
| `[[Glossary#Renown]]` | [[Glossary#Renown]] | The term's heading, which opens the entry |
| `[the glossary](#/glossary)` | [the glossary](#/glossary) | The whole glossary |
| `[A to Z](#/glossary?group=az)` | [A to Z](#/glossary?group=az) | The glossary, listed A to Z |

The second form is checked: the page check reports a term that is not in the glossary.
