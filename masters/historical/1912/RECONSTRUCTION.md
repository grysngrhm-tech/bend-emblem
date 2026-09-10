# The 1912 historical family — reconstruction record

Content doctrine §5: a master with an unlisted change is not a
reconstruction. This is the list.

## What this is

Two SVG masters of the Bend Emblem **as printed in the Bend Bulletin of
3 July 1912** — the earliest publication of the mark this project has
located (`archive/newspapers/bend-bulletin/1912-07-03-*`, source id
`bb-1912-07-03`).

This is a **separate family** from the modern/common masters in
`assets/emblem/masters/`. It does not replace them and nothing about them
was touched. The visual difference between the two is part of the history,
not an error in either.

| | 1912 historical | Modern / common (v1.1) |
|---|---|---|
| Border | **Double ring**: an outer keyline and an inner ring | Single solid disc edge |
| Letterforms | Irregular, hand-composed; pointed B counters, flared E, asymmetric N, compressed D | Regularised, even strokes |
| Ink inside the disc | **72%** in the source, 70% in this reconstruction | 50% |
| Central symbol | A small circled © is visible in the newspaper — **not reproduced here**, see below | None |

The ink figures were measured on 2026-09-10 by sampling the disc interior
of the archive's own page image against each rendered master. They are the
evidence that this reconstruction is faithful to its source and that the
modern family is a different drawing, not a cleaner version of the same one.

## Classification

**Historical reconstruction.** Unlike the modern/common family, this one has
an identified specimen: the Bend Bulletin of 3 July 1912, filed at
`archive/newspapers/bend-bulletin/1912-07-03-*` and readable at
[Historic Oregon Newspapers](https://oregonnews.uoregon.edu/lccn/sn96088235/1912-07-03/ed-1/seq-28/).
The reconstruction changes nothing beyond removing reproduction noise and
normalising the frame; the list of what was and was not changed is below.
This is the distinction VISION.md §8 asks for, and it can be made truthfully
for the first time here.

## Where it came from, and what was changed

Derived from the package Grayson supplied on 2026-09-10, filed verbatim and
unedited at `archive/emblem-packages/1912-historical/`, whose own SHA-256
manifest was verified file by file (32 of 32 match).

That package's masters trace the **whole advertisement** — the top rule, the
emblem, every line of the notice, and the bottom ornaments — as one path of
93 subpaths and 580 KB. `scripts/extract-1912-master.mjs` selects the six
subpaths that fall inside the emblem's own bounding box, bakes a
translate-and-scale into their coordinates so the mark fills the standard
`viewBox="0 0 1000 1000"`, and writes these two files. Nothing else was
altered: no smoothing, no regularising, no reversing of curves. Re-run the
script to reproduce them exactly.

Kept: 6 subpaths — the outer ring, the inner ring, the letter mass, the two
B counters and the D counter. Dropped: 87 subpaths of newspaper furniture.

## The central copyright symbol — decided: it stays off

The 1912 specimen carries a small circled **©** in the white channel between
the E and the N. It is plainly visible in the page image and it is the
typographic counterpart of the notice printed beneath the mark: *"The above
brand is copyrighted."*

**It is not in these masters.** The supplied trace never captured it, and on
2026-09-10 Grayson decided it stays off.

The reasoning, recorded so it is not relitigated: a © glyph sitting on a mark
this project exists to give away says the opposite of what the project means,
and the licensing review has not recorded an outcome (AGENTS.md rule 3). The
symbol is not being hidden — the page image on
[its archive record](/archive/bb-1912-07-03/) shows it plainly, the
reconstruction is displayed beside that page, and this record says the mark
carried one. What the site does not do is reproduce it on files people are
invited to cut, print and paste.

If that is ever reversed, the symbol must be traced from the specimen rather
than drawn from a modern font, and this section rewritten.

## What the supplied package's documentation says, and where it is wrong

Recorded because the package is filed in the archive and a later reader will
otherwise trust its README. Verified 2026-09-10:

1. **"Archival Reconstruction — retains the observed central copyright
   symbol."** It does not. The symbol is absent from the geometry.
2. **"Usage Master — removes only that symbol."** The usage and archival
   masters are **byte-identical in path data** (both 580,281 characters, and
   their renders differ by zero pixels). They differ only in `<title>`,
   `<desc>` and `data-` attributes. There is one drawing, not two.
3. **The derived files are all of the whole page**, not the emblem: the PNGs
   at 512–4096, the WebP, the PDF and EPS, the DXF and cut-path SVG, and the
   favicons. The 32 px favicon is an illegible smudge.

None of this makes the package worthless — its trace of the emblem is good,
and it is the reason this family exists. But its own structural checks all
passed, which is upstream guards rule 9: existence is not fitness. Render the
thing before trusting it.

## Not done yet

- These masters are **not** wired into the emblem package build, so they do
  not appear on `/download/` and no `/emblem/1912-*/` asset paths exist.
  Adding a second family to the download library is Grayson's call.
- No PNG, PDF, EPS or DXF derivatives are generated from them.
- The © decision above.
