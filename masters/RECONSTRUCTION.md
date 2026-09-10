# Reconstruction record

What each master is, what it was traced from, and what was changed.
Content doctrine §5: a master with an unlisted change is not a
reconstruction. Filed 2026-09-10 from the v1.0 package; the package's
own account of derivation is one sentence, quoted below, so most of
this record is open.

## The five masters (v1.0)

| File | Variant | Fills | Notes as received |
|---|---|---|---|
| `bend-emblem-original.svg` | Original: black emblem on a white field | `#000000` on a `#FFFFFF` `<rect>` | The only master with a background rectangle. VISION.md §7 describes the Original as the solid circle with BEND knocked out; this file is that circle placed on a white field. |
| `bend-emblem-cutout-black.svg` | Cutout Black: black circle, letters transparent | `#000000` | Same path data as Original minus the rect. |
| `bend-emblem-cutout-white.svg` | Cutout White (the "Reverse" of VISION.md §7): white circle, letters transparent | `#FFFFFF` | Same geometry, fill flipped. |
| `bend-emblem-lettermark-black.svg` | Lettermark Black: the four letters only | `#000000` | Different path set (the letters as positive shapes). |
| `bend-emblem-lettermark-white.svg` | Lettermark White | `#FFFFFF` | Same geometry, fill flipped. |

All five: `viewBox="0 0 1000 1000"`, no strokes, no text elements, no
embedded rasters, single-fill paths. Two departures from the master
rules in handbook `emblem-package.md` §2, recorded rather than fixed:
each carries `width="1000" height="1000"` alongside the viewBox, and
none yet carries `<title>`, `<desc>`, or a `data-emblem` attribute.
Fix them in a v1.1 with an entry below.

## Classification

**Undetermined.** The package README says: "These files are a cleaned
digital reconstruction derived from the preserved Bend Emblem artwork.
They are intended to preserve the historic form while providing
technically clean modern files. Future archival research may justify a
separately labeled historical reconstruction based directly on an
earlier primary-source specimen."

So v1.0 is, in this project's terms, a **modern optimized** set whose
fidelity to a primary specimen has not been checked, because the
specimen is not identified. Until `archive/logo-reference/` holds the
specimen and a comparison is recorded here, the site labels these files
as the modern reconstruction and does not call them the historical
reconstruction.

## Open

- **Traced from:** which artwork? Where is it, who holds it, and is
  there a scan? (`archive/logo-reference/` is empty.)
- **Method:** manual trace, auto-trace with cleanup, or redrawn? The
  path data (absolute `L` segments at two-decimal precision, ~10 KB per
  circle) reads like a cleaned auto-trace; confirm with the author.
- **Changes from the specimen:** unknown until the specimen exists.

## Revisions

| Date | Version | Change |
|---|---|---|
| 2026-09-09 | v1.0 | Package generated (manifest.json `generated` date). |
| 2026-09-10 | — | Filed as received; nothing changed. |
| 2026-09-10 | v1.1 | The five masters brought to the handbook §2 rules, geometry untouched: `width`/`height` dropped (viewBox only); `<title>`, `<desc>` and `data-emblem="optimized"` / `data-variant` added (optimized, because the classification above is undetermined and the site must not call these the historical reconstruction). One change to `bend-emblem-original.svg`: the v1.0 white field was a full 1000×1000 `<rect>`, so every transparent-format derivative of the Original carried a white square; the v1.1 field is the emblem's own outer contour (the first subpath of the black path, filled white, under it), so the letters stay white and the corners are transparent. The JPG-on-white derivative is unaffected. `package-v1.0/` keeps the v1.0 files untouched. |
