# The Bend Emblem

A solid disc with **BEND** knocked out of it. It was printed across a full
page of the Bend Bulletin on **3 July 1912**, and the men of the Bend
Emblem Club swore in January 1913 to wear it every day "until Bend has a
population of one hundred thousand."

This repository holds the vector masters and the complete package built
from them, mirrored from **[BendEmblem.com](https://bendemblem.com)**,
which is canonical.

## Use it

**The emblem is free to use. No permission required.**

Put it in your window. Print it on a shirt. Make a sticker. Cut it from
steel. Engrave it in wood. Use it on your website. Paint it on a wall. Put
it on your car. Put it somewhere nobody has thought of.

That is not a modern reinterpretation of the club's intent. It is the
intent. The club handed small printing cuts of the emblem to the editor of
the Bend Bulletin so members could drop it into their advertisements, their
cheques and their stationery, and hoped aloud that the next issue would
"look as if it had the emblematic measles." In June 1922 the club gave the
Bend Commercial Club leave to use the emblem "in any way it sees fit," and
the Bend Iron Works started casting it in aluminium for cars.

## What is here

```text
masters/      five SVG masters + RECONSTRUCTION.md
package/      60 files built from those masters
  original/ cutout-black/ cutout-white/ lettermark-black/ lettermark-white/
  web/        favicons (SVG, ICO, 180, 192, 512) and the web manifest
  maker/      DXF and cut-path files
  package/    manifest.json — every file with its bytes and SHA-256
datapackage.json   Frictionless Data descriptor
CITATION.cff       how to cite this, if you want to
CHANGELOG.md       dated snapshots; v1.1 is the first
```

Which file do you want?

| You are | Take |
|---|---|
| Putting it on a website | `package/*/…​.svg`, or `package/web/` for favicons |
| Printing it | the PDF or EPS in the variant folder |
| Cutting, engraving, CNC, vinyl | `package/maker/` and the **cutout** variants, whose letters are real transparent knockouts rather than white shapes |
| Putting it on a dark background | the **cutout-white** variant |
| Just want the mark, no disc | the **lettermark** variants |

Everything in `package/` is computed from `masters/` by the build script in
the [BendEmblem.com repository](https://github.com/grysngrhm-tech/BendEmblem),
and `package/package/manifest.json` gives a byte count and a SHA-256 for
every file, so you can check what you downloaded.

## Reconstruction, not a scan

These files are a **modern reconstruction** of the historic mark, not a
photograph or a scan of the original artwork. The specimen they were traced
from has not been identified, so the package does not claim to be a
faithful historical reconstruction — it says its classification is
undetermined, and `masters/RECONSTRUCTION.md` records exactly what is known
about how they were made and what was changed.

The earliest published emblem now on hand is the
[Bend Bulletin of 3 July 1912](https://oregonnews.uoregon.edu/lccn/sn96088235/1912-07-03/ed-1/seq-28/).
Comparing these masters against it is the next thing to do.

## Using it

**Free to use. No permission required.** That is the whole message, and it
is the message the historical record supports.

You will notice there is **no `LICENSE` file in this repository, and no
licence named anywhere in it.** That is deliberate, and it is not an
oversight to be tidied up by adding one.

The emblem was published in 1912 with the words "The above brand is
copyrighted" beneath it. A provenance review is underway in the
BendEmblem.com repository
([`docs/research/licensing.md`](https://github.com/grysngrhm-tech/BendEmblem/blob/main/docs/research/licensing.md))
to establish what that means today, and it is not finished. Stamping a
licence on a mark before knowing what rights exist in it — including the
possibility that none do, and that no licence is any of our business to
grant — would manufacture exactly the ambiguity the review exists to
remove. So the repository says what it can stand behind: use it freely, and
nobody here will ask you for permission.

When the review records an outcome, this file, `CITATION.cff` and
`datapackage.json` get updated together, in one change, and a release is
tagged.

## Citing it

You do not have to. If you want to, `CITATION.cff` has the details, or
simply link **https://bendemblem.com**.

## The history

The story, the sources and the 1913 book are at
[bendemblem.com](https://bendemblem.com) — every claim cited to a document,
and a note wherever the sources disagree.

The site revives the emblem, not the club. It is not the Bend Emblem Club,
not its successor, and not a City of Bend project.
