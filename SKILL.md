---
name: poster-ready-plots
description: Make matplotlib figures poster-ready with 18-24 pt text, sparse ticks, SVG + PNG exports, and poster-panel layouts that stay readable at poster scale without overlaps between labels, axes, legends, titles, panels, or plotted marks.
---

# Poster Ready Plots

## When To Use

Use this skill when a matplotlib figure, plot grid, or report graphic needs to stay readable at poster scale.

## Defaults

- Use 18 pt as the body baseline, 20 pt for axis labels and panel titles, and 24 pt for figure titles.
- Prefer sparse numeric ticks over dense tick labels. Keep the tick count low before shrinking text.
- Keep legends outside the data area when they compete with the plot.
- Reserve dedicated space for titles, subtitles, and legends in dense multi-panel figures.
- For multi-panel figures, prefer building each panel cleanly first, then assembling and adjusting the combined layout.
- Keep all figure text editable in the exported output when possible, ideally as native text in SVG/PDF rather than converted to paths, especially for labels, titles, and legends.
- Always check that axis labels, tick labels, legends, titles, panel borders, and plotted marks do not overlap each other before considering the figure done.
- Prefer a single visual encoding for emphasis when possible. If a mark needs to be smaller or larger, encode that directly rather than stacking a smaller overlay on top of a full-size mark.
- Export SVG as the primary archival format and keep PNG alongside it for compatibility.
- Use 300 dpi for raster export and for any rasterized content embedded in SVG.

## Workflow

1. Start from a normal poster-panel figure size instead of a screen-sized or oversized canvas.
2. Reflow dense layouts before reducing text size.
3. Split a figure into companion views if a single canvas cannot hold the target typography cleanly.
4. Check for clipping, cramped titles, cramped legends, and over-labeled axes.
5. Verify that labels, axes, legends, titles, panels, and plotted data do not overlap each other in the final render.
6. If the layout still needs smaller-than-target text, treat that as a signal to simplify the figure.

## Quick Checks

- Axis labels should read larger than tick labels.
- Multi-panel figures should still have breathing room between panels.
- Title stacks should not overlap panel titles or legends.
- Labels, axes, legends, titles, panels, and plotted marks should not overlap each other.
- If emphasis is shown by size, the mark itself should change size rather than getting an overlay on top.
- Numeric axes should usually show only a handful of labels.
- SVG and PNG outputs should share the same stem.
