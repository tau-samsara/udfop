---
title: Demo: Quotes
category: Site Guide
summary: Quotations, nested content in a quote, and how a quote differs from a notice box.
authors: tau
---

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

## A quotation

> "A quotation starts each line with a greater-than sign."
> Several lines stay in one quote.

## Quotes can hold other things

> A quote can hold a list:
>
> - one
> - two
>
> and **formatting**, and a [[Controls|link]].

## Attribution

> Mastered skills can reach level 200.
>
> From the release notes, patch 0.1.4991

## Not the same as a notice box

A quotation whose first line is a tag such as `[!NOTE]` becomes a notice box (see [[site:Demo: Notice boxes]]). An unknown tag leaves an ordinary quote, and the page check mentions it:

> [!DANGER]
> This is a quotation, not a box, because the site does not know DANGER.
