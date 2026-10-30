---
title: Demo: Pictures
category: Site Guide
summary: Plain pictures, captions, floating left and right, centering and widths.
authors: tau
---

> [!TIP]
> To see the Markdown this page is written in, open its **View Source** tab at the top of the page.

## A plain picture

![A placeholder picture](../placeholder.svg)

Readers can click any picture to open it, move through the pictures of the page, and zoom in.

## A caption

A caption in quotes after the path frames the picture and floats it to the right, 240 pixels wide. The picture has to be alone on its line.

![A placeholder picture](../placeholder.svg "A caption names what the picture shows."){right}

Text next to a floated picture wraps around it. This paragraph runs down the left of the picture above, and a heading starts below it, so the page stays tidy. On a phone the picture moves above the text and takes the full width.

## Floated left

![A placeholder picture](../placeholder.svg "Floated left, 150 wide."){left 150}

The same idea on the other side: a small picture beside the paragraph it illustrates. Several pictures floated the same way stack down the side, and the text carries on beside them for as long as there are lines to fill.

## Centered

![A placeholder picture](../placeholder.svg "Centered, 400 wide."){center 400}

## A width and no caption

![A placeholder picture](../placeholder.svg){right 120}

Braces alone, with a side and a width, float a picture without a caption. The width is from 40 to 1200 pixels, and a picture never grows past its own size.
