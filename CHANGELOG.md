# Changelog

Dated snapshots of the Bend Emblem masters and the package built from
them. The package is computed from the masters by
`scripts/build-emblem-package.mjs` in the
[BendEmblem.com repository](https://github.com/grysngrhm-tech/BendEmblem);
nothing in `package/` is hand-made, and `package/package/manifest.json`
carries a byte count and a SHA-256 for every file.

## v1.2 — 2026-09-10

**A second family: the 1912 emblem.** Until now this repository held one
drawing. It now holds two, and they are not two renderings of the same
thing.

```text
masters/
  historical/1912/   the 1912 emblem, black and white
  modern/            the five v1.1 masters, unchanged
```

| | 1912 | Common (v1.1) |
|---|---|---|
| Source | The Bend Bulletin, 3 July 1912 — [read the page](https://oregonnews.uoregon.edu/lccn/sn96088235/1912-07-03/ed-1/seq-28/) | Not identified |
| Classification | **Historical reconstruction** | **Undetermined** |
| Border | Double ring | Single disc edge |
| Ink inside the disc | 72% in the source, 70% reconstructed | 50% |

The 1912 emblem is the earliest published form of the mark the project has
found: a full newspaper page carrying it above the line *"The above brand is
copyrighted. The Bend Park company, to whom it belongs…"*. Because its
specimen is identified, it can be called a historical reconstruction — which
the common family still cannot, since the artwork behind it has never been
located. Measured against the newspaper page, the two are demonstrably
different drawings, so neither replaces the other.

**The central copyright symbol is not reproduced.** The 1912 specimen carries
a small circled © between the E and the N. It is visible on the archive page
and recorded in `masters/historical/1912/RECONSTRUCTION.md`, and deliberately
left off files that people are invited to cut, print and paste: a copyright
glyph on a mark being given away says the opposite of what this is for.

**No PDF or EPS for the 1912 family.** The build has no vector converter and
the supplied print vectors traced the whole advertisement rather than the
mark. The manifest declares the absence and says why rather than dropping the
format silently. The SVG is the master; any print shop can take it.

**Nothing about the v1.1 masters changed.** Same files, same bytes, same
`/emblem/original/…` paths. The later mark is now *titled* "Common Emblem"
rather than "Original" on the website, since calling it the original beside a
1912 drawing would be wrong, but its id and every published path are
untouched.

Package: 7 variants, 75 files.

## v1.1 — 2026-09-10

First snapshot in this repository. Superseded by v1.2, which adds the 1912 family; these masters are unchanged by it.

**Masters (`masters/`).** Five SVGs, `viewBox="0 0 1000 1000"`, single-fill
paths, no strokes, no text elements, no embedded rasters:

| File | What it is |
|---|---|
| `bend-emblem-original.svg` | Black emblem on a white field |
| `bend-emblem-cutout-black.svg` | Black disc, letters as real transparent knockouts |
| `bend-emblem-cutout-white.svg` | White disc, letters knocked out (for dark grounds) |
| `bend-emblem-lettermark-black.svg` | The four letters only, black |
| `bend-emblem-lettermark-white.svg` | The four letters only, white |

Changes from v1.0, each recorded in `masters/RECONSTRUCTION.md`:

- Added `<title>`, `<desc>` and a `data-emblem` attribute to every master.
- Dropped the `width`/`height` attributes, keeping the `viewBox`, so the
  files scale cleanly wherever they are placed.
- **One geometry-adjacent change:** the Original's white field is now
  clipped to the outer contour. In v1.0 it was a full-square field, which
  gave every transparent derivative white corners.

**Package (`package/`).** 60 files built from those masters: SVG, PNG at
256/512/1024/2048/4096, JPG, WebP, PDF, EPS, DXF, favicons (SVG, ICO, 180,
192, 512) and a web manifest. PDF, EPS and DXF ship as supplied with v1.0
rather than computed, because the build does not yet carry a vector
converter; the manifest says so per file.

**Not here yet, deliberately:**

- No `LICENSE` file and no licence named anywhere. See "Using it" in the
  README.
- No release tag and no Zenodo DOI. Both wait on the same review.
- No 8000 px archival raster. It is 2 MB per file and belongs in a
  snapshot, not in every deploy; it will land here when it is generated.

**Classification: undetermined.** These are a modern reconstruction of the
historic mark, but the specimen they were traced from has not been
identified, so the package does not claim to be a faithful historical
reconstruction. The earliest published emblem now on hand is the
[Bend Bulletin of 3 July 1912](https://oregonnews.uoregon.edu/lccn/sn96088235/1912-07-03/ed-1/seq-28/);
comparing the masters against it is the next step.
