# Playmos Brand Kit

The official Playmos Labs brand assets in a repo-ready, machine-readable layout. People and AI tools (bots, codegen, design agents) should read the JSON files here instead of guessing colors or fonts from screenshots.

Updated 2026-10-21. Hex values and fonts were verified from the `playmos-labs/website` source code. Usage rules were approved by Boz on Oct 21, 2026. The human-readable copy lives in Google Drive under Grok Bot > 06 Design > Brand Kit. This folder is laid out to mirror the GitHub repo `playmos-labs/brand-assets` (https://github.com/playmos-labs/brand-assets).

## Layout

```
.
├── README.md                     this file: layout, usage rules, rights
├── logos/
│   ├── manifest.json             every logo file, what it is, when to use it
│   ├── primary/                  the primary logo (full-color mark) only
│   └── alternates/               white, dark, icon-only, horizontal lockups
├── colors/
│   ├── brand-colors.json         ONLY primary + secondary brand colors
│   └── alternate-colors.json     extended scales, neutrals, accents, partner, superseded
└── typography/
    ├── fonts.json                families, weights, CSS stacks, licenses, type scale
    └── fonts/                    Geist + Geist Mono variable TTFs and the OFL license
```

## For AI tools

The JSON files are the machine-readable source of truth. Read colors from `colors/brand-colors.json` (primary and secondary only) and `colors/alternate-colors.json` (extended scales, neutrals, accents). Read type from `typography/fonts.json`. Look up logo files in `logos/manifest.json`; every `file` path there is relative to this repository root.

Use `colors/brand-colors.json` by default. Reach for `colors/alternate-colors.json` only for UI states, neutrals, charts or illustrations. Use `logos/primary/` by default and `logos/alternates/` only when the background calls for it (see below).

Coral is standardized on #FF5C7A (Boz, Oct 21, 2026). #FF5C57 from the website's Tailwind config is superseded, and Derek's team should update `tailwind.config.ts` to #FF5C7A.

Each color entry has `name`, `hex`, `rgb`, `role`, `usage`, `source` (the file in the website repo) and `status`.

## Logos

- **Primary:** `playmos-logo-fullcolor.svg`, plus transparent PNGs at 1024 and 512 px. `playmos-logo.svg` and `playmos-logo.png` are the official logo from the website repo (`public/brand-assets`), with one correction: in the original file the two button dots were stroked and merged into an "8". Per Boz on Oct 21, 2026, they now use `stroke="none"` and render as two separate dots, as in the playmos.io nav. The PNG keeps the original's 1025 px size and white background.
- **Alternates:** `playmos-logo-white`, `playmos-logo-dark` (#0A0C12), `playmos-logo-icon-only` (violet controller), `playmos-logo-icon-only-white`, `playmos-logo-horizontal` (dark wordmark), `playmos-logo-horizontal-white`. Each comes as an SVG plus 1024 and 512 px transparent PNGs.
- **Every** logo file uses the two-separate-dots controller (circle `stroke="none"`), approved by Boz on Oct 21, 2026. Don't use older files with a merged "8".
- There is no stacked lockup yet (optional, pending).

## Usage rules (approved by Boz, Oct 21, 2026)

- **Clear space:** leave 0.25x the mark's height empty on every side.
- **Minimum size:** mark 24 px on screen / 8 mm in print; icon-only 16 px; horizontal lockup 96 px wide / 25 mm.
- **On dark (#0A0C12, #11151E):** full color, horizontal-white, icon-only (violet or white).
- **On white or light:** full color, horizontal, dark, icon-only (violet).
- **On violet (#635BFF):** white or icon-only-white. Never full color.
- **On photos or busy art:** put the logo on a solid or blurred dark panel, or use white on a dark overlay of at least 60%.
- **Don't:** stretch, recolor, rotate, add effects (shadow, glow, outline, 3D), crop the rounded square, rearrange or retype the lockup, place it on busy or low-contrast backgrounds, or combine it with partner marks (Base Blue #0052FF belongs to Base).
- **Accessibility:** small text needs at least 4.5:1 contrast. On #0A0C12 use #A99FFF or #8478FF for small violet text (#635BFF is 4.2:1, so large text only). White on #635BFF is 4.7:1. Teal #0FB67E on white is 2.6:1, so don't use it for text on white. Never rely on color alone.

## Rights

Copyright (c) 2026 Playmos Labs. All rights reserved.

Logos and marks are Playmos trademarks, all rights reserved, usable only to refer to Playmos. The Playmos name, the Playmos logo and the controller mark are trademarks of Playmos Labs. No license to use them is granted by this repository, except for authorized use by Playmos Labs, its team, contractors and approved partners in line with these rules. Don't modify the marks, imply endorsement or partnership, or use them in your own branding without written permission.

The fonts in `typography/fonts/` (Geist, Geist Mono, Copyright (c) 2023 Vercel, in collaboration with basement.studio) are third-party and licensed separately under the SIL Open Font License 1.1 (`typography/fonts/OFL-LICENSE.txt`). The all-rights-reserved notice above does not apply to them.
