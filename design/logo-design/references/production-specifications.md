# Logo Production Specifications

Read this reference before building final artwork, exporting assets, or auditing a production logo package.

## Contents

- [Master Artwork](#master-artwork)
- [Required Variants](#required-variants)
- [Clear Space](#clear-space)
- [Minimum Size](#minimum-size)
- [Color Specifications](#color-specifications)
- [Export Formats](#export-formats)
- [File Naming](#file-naming)
- [Package Structure](#package-structure)
- [Usage Sheet](#usage-sheet)
- [Verification](#verification)
- [Delivery Notes](#delivery-notes)

## Master Artwork

Build the approved logo as vector artwork whenever the form permits. Keep one editable master and derive all variants from that source.

For SVG masters:

- Use a correct `viewBox` and intentional bounds.
- Remove stray objects, hidden artwork, clipping accidents, and unnecessary editor metadata.
- Avoid external image links, external CSS, scripts, and remote font dependencies.
- Use clean paths with economical anchor points.
- Preserve fills and strokes intentionally; expand strokes when production consistency requires it.
- Keep a live-type editable source when possible and an outlined distribution version when font substitution is a risk.
- Do not embed raster imagery unless the approved identity explicitly requires it.

For PDF masters, preserve vector paths and embedded or outlined type. Do not create a PDF that merely wraps a low-resolution PNG.

## Required Variants

Create only the variants needed by the brief. A full package commonly contains:

- `primary`: preferred lockup
- `secondary-horizontal` or `secondary-stacked`
- `mark`: symbol only
- `wordmark`: name only
- `one-color-black`
- `one-color-white`
- `reverse`: version optically corrected for dark backgrounds when necessary
- `small`: simplified version for tiny applications
- `app-icon` or `favicon`: only when requested or relevant

Do not use a white rectangle behind a reversed logo. The background should remain transparent unless a containing shape is part of the approved design.

## Clear Space

Define clear space from a stable feature in the logo, such as the cap height, symbol module, or a specific counter width. Name the unit `x` and state the minimum exclusion zone on every side.

Clear space is a minimum, not a layout recommendation. Verify that the chosen unit remains meaningful across every lockup.

## Minimum Size

Determine minimum size through rendering tests, not convention alone. Test at realistic pixel and print sizes and stop reducing when counters close, letterforms become ambiguous, or the recognition feature disappears.

Document minimum width separately for full lockup, symbol, and small-size variant. Common screen tests include 16, 24, 32, 48, 64, 128, and 256 px, but only retain sizes relevant to the actual use case.

## Color Specifications

Use exact values taken from the approved artwork:

- `HEX` and `RGB` for screen use
- `CMYK` for print only after a real color conversion and visual review
- Spot or Pantone references only after an actual match; never guess

Use sRGB for ordinary PNG exports unless another profile is explicitly required. Check the mark on white, black, the primary brand color, and representative light and dark surfaces.

## Export Formats

Default final formats:

- `SVG`: primary scalable digital master
- `PDF`: vector print and sharing format
- `PNG`: transparent raster exports for common digital use

Add `EPS` only for a confirmed legacy production requirement. Add `JPG` only for applications that cannot support transparency. Do not imply that a bitmap format is a vector master.

For PNG, export useful fixed widths based on the application. A general package may use 256, 512, 1024, and 2048 px for the primary lockup and 32, 48, 128, 256, 512, and 1024 px for a square mark. Avoid generating dozens of redundant sizes.

## File Naming

Use lowercase hyphenated filenames with a predictable sequence:

`brand-variant-color-background.ext`

Examples:

- `northstar-primary-full-color-light.svg`
- `northstar-primary-black-transparent.png`
- `northstar-mark-white-transparent.svg`
- `northstar-small-full-color-light.png`

Use the actual brand slug and omit fields that add no information. Keep naming identical across formats.

## Package Structure

For a full identity package, use a structure similar to:

```text
brand-logo-package/
├── master/
│   ├── editable-source
│   ├── brand-primary.svg
│   └── brand-primary.pdf
├── svg/
├── pdf/
├── png/
│   ├── light-background/
│   └── dark-background/
├── favicon/
└── brand-logo-usage.pdf
```

Include only folders with actual deliverables. Do not create empty directories or legacy formats that were not requested.

## Usage Sheet

Keep the usage sheet concise and visual. Include:

- Primary and alternate lockups
- Color values
- Clear-space construction
- Tested minimum sizes
- Correct light and dark background usage
- A short list of meaningful misuses
- Typeface name and licensing dependency when relevant

Do not fabricate broad brand guidelines when only a logo has been approved.

## Verification

Render each SVG and PDF to a bitmap preview and inspect it. Check both the entire composition and small-size crops.

Verify:

- Correct brand spelling and variant labels
- Expected dimensions and transparent backgrounds
- Consistent proportions and clear space
- No clipping, missing shapes, substituted fonts, or broken links
- Clean curves, joins, counters, and optical alignment
- Equivalent visual weight across positive and reversed versions
- Legibility at the documented minimum size
- Valid opening in at least one independent renderer when available
- Vector preservation in SVG and PDF files
- No accidental metadata, hidden concepts, or unlicensed assets in delivery files

When possible, compare file hashes or generate the package from one master to prevent stale variants. Re-export any file that fails inspection; do not patch a raster preview and leave the vector source incorrect.

## Delivery Notes

State:

- Which logo direction is approved
- Which files are editable masters and which are distribution exports
- Which fonts or licenses are required
- Which color spaces are included
- What minimum-size testing was performed
- Whether trademark screening occurred, while clearly distinguishing it from legal clearance
- Any format or production limitation that remains
