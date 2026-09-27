# Review-ready A0 poster audit

Canonical repository: <https://github.com/dku-comsci-econ206-Autumn2026/FP10-StayOrSwitch-Yiqiao>

Audit date: 2026-09-27 (Asia/Shanghai)

Paper baseline: `43a2941184d8130852af3c1f88fc90e8b2fd9fc6`

Historical model/output baseline: `f9523b0`

Official team code: FP10

## Deliverables and template provenance

- Editable poster: `submission/PS2-FP10-StayOrSwitch-A0-Poster.pptx`
- Print export: `submission/PS2-FP10-StayOrSwitch-A0-Poster.pdf`
- The prior review-ready filenames are preserved with byte-identical updated content.
- Official source: `/Users/mickeyxiaoliuliu/Desktop/DKU curriculums/cs206/ps2的一些模版/COMSCI_ECON206_PS2_A0_Poster_Template.pptx`
- Official-source SHA-256: `2c0bfad24ded809e845d01fd94b814abc4486d431731e0562b24d7bf8f9c0b58`
- The official one-slide layout, DKU logo, three-column structure, key-message band, footer structure, brand colors, and A0 geometry were retained. Template-fidelity validation reported coverage ratio `1.0` against a required minimum of `0.7`.

## Geometry and file integrity

| Check | Result |
|---|---|
| PPTX slide count | 1 |
| PPTX slide size | `42804000 × 30276000` EMU = `1189 × 841 mm` landscape |
| PDF page count | 1 |
| PDF media box | `3370.3937 × 2383.9370 pt` = `1189 × 841 mm` (A0 landscape) |
| PPTX SHA-256 | `24d6c164ae41ca39d6695c1277de88f690259c2176908160bdb66cbd6f1eed25` |
| PDF SHA-256 | `757e719655862cdc386958f94ab141a76b3acdadab0f39a1731befb44b29feee` |
| First-party PPTX re-import | Pass; one slide; byte hash matched the finalized artifact |
| Package integrity | Pass; zero findings |

## Visual and typography QA

- The finalized slide passed first-party re-import and automated geometry QA. The PDF was independently rendered at `7022 × 4967` pixels and visually inspected.
- No clipped title, body, table, footer, logo, URL, or QR content was observed. No unintended object overlap or off-slide object was found.
- Automated presentation-layout validation reported zero findings and zero warnings, including heading-fit and bullet-geometry checks.
- The result matrix is a native editable PowerPoint table; the Economics → Computation → Behavior figure is composed of native editable PowerPoint shapes and connectors.
- All 112 checked text runs in the PPTX use the official template's Calibri family. Native Calibri rendering could not be verified in the export environment. Consistent with the template's own note, the PDF embeds metric-compatible Carlito/Carlito Bold; its rendered layout was therefore checked separately.
- The smallest footer text follows the official template's dense reference/footer treatment and remained present in both renderings. It is intended for close reading, while the main content preserves poster-scale hierarchy.

## Link and QR verification

The following public URLs returned HTTP 200 on 2026-09-27:

- GitHub repository: <https://github.com/dku-comsci-econ206-Autumn2026/FP10-StayOrSwitch-Yiqiao>
- Hugging Face Space: <https://huggingface.co/spaces/mickeystk/ps2-stay-or-switch-memory-portability>
- Rendered Space endpoint: <https://mickeystk-ps2-stay-or-switch-memory-portability.static.hf.space/index.html>

Both full URLs are visible and clickable in the PPTX and PDF. Both source QR PNGs decoded exactly to their printed URLs. After PDF export, both codes were decoded again from a 150-dpi full-page rasterization of the PDF. The codes occupy approximately 32 mm square on the A0 page. The public Space README was also updated at revision `751f5cd` so its source-project link resolves to the same canonical repository.

## Cross-artifact parity

| Poster claim | Paper/output source | Parity result |
|---|---|---|
| Exactly two pure BNE: `(LL,LL)` and `(PL,PL)` | `paper/sections/proposal.tex`; `outputs/benchmark_verification.json` | Match |
| Low-type mixed probability `6/7` | `paper/sections/proposal.tex`; `outputs/symmetric_mixed_equilibrium_p_sweep.csv` | Match |
| Welfare at `m=1`: `0`, `2.17`, `4`; `PP` is a comparator | paper main text and Appendix C | Match; non-equilibrium status retained |
| At `p=.4`, `tau=.4` weakly sustains `PL`; `LL` remains weak through `tau=1.2` | `outputs/mechanism_thresholds.json`; paper main text | Match; weak-boundary language retained |
| Allocation `.75193` at `r=.50` and `.96004` at `r=.20` | `outputs/auction_summary.csv`; `outputs/auction_validation.json` | Match |
| `N=100,000`, seed `20603`, conditional efficiency `1` | paper main text and Appendix F; auction outputs | Match |
| Twelve fixed scenarios, six Stay/six Switch | `outputs/behavioral_validation.json`; behavioral artifact | Match |
| Page-session aggregation only; no participant conclusion | paper main text; behavioral evidence boundary | Match |
| `85/85` tests | Full `cs206-ps2` environment test run on 2026-09-27 | Pass: 85 tests |

The poster does not claim participant behavior, classroom auction play, symposium feedback, causal impact, market calibration, optimal-auction design, or resolved equilibrium selection. It keeps observed/computed results separate from the planned user test and symposium question.

## Reproduction

- `poster/build_poster.mjs` imports and edits the official template using the presentation artifact tooling, adds the native table/diagram and QR assets, and finalizes the PPTX under the template and geometry contracts.
- `poster/generate_qr.mjs` regenerates the two QR PNG assets from the displayed public URLs.
- The PDF was exported from the finalized PPTX with LibreOffice Impress and then independently checked for A0 media-box geometry, text presence, hyperlinks, raster layout, and QR decodability.

## Manual items not invented

- The official team code is FP10.
- No symposium session identifier is supplied.
- Human approval of the final wording and any later peer/symposium feedback remain the author's responsibility.
