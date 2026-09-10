# Changelog

Dated snapshots of the Bend Emblem masters and the package built from
them. The package is computed from the masters by
`scripts/build-emblem-package.mjs` in the
[BendEmblem.com repository](https://github.com/grysngrhm-tech/BendEmblem);
nothing in `package/` is hand-made, and `package/package/manifest.json`
carries a byte count and a SHA-256 for every file.

## v1.1 — 2026-09-10

First snapshot in this repository.

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
