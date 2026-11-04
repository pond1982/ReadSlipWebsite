# ReadSlip development-build screenshots

These PNGs are unmodified copies of actual native SwiftUI/UIKit test captures from
[ReadSlip commit 83e836f35161ba01ee94cc795d4b7553fb727718](https://github.com/pond1982/ReadSlip/commit/83e836f35161ba01ee94cc795d4b7553fb727718),
version **1.2 (9)**, captured on November 4, 2026. They illustrate the tested free
redesign; they do not establish that this version is publicly available on the
App Store.

| Website asset | Original path under `Launch/NativeRedesignQA/` | Capture |
| --- | --- | --- |
| `overview.png` | `build9-overview-pip-390-light.png` | Overview, daily/weekly/monthly controls, synthetic totals and Pip; 780 × 1688 px |
| `bulk-review.png` | `build9-bulk-20-selected-390-light.png` | Actual bulk-classification toolbar fixture with 20 selected drafts; 780 × 1688 px |
| `free-settings.png` | `build9-settings-pip-390-light.png` | Free local access, separate earlier-subscription management and export entry; 780 × 1688 px |
| `accessibility-direction.png` | `build9-direction-320-accessibility-dark.png` | Actual direction-selector component fixture with large accessibility text in dark appearance; 640 × 1688 px |

The captures use the app's native views inside a fixed 390 × 844 point viewport
(standard text), or a 320 × 844 point viewport (accessibility3 text), at 2× scale
in the available iPhone Duo simulator runtime. They are fixed native viewport
checks, not physical-device screenshots or emulation of another iPhone model.
Only the visible viewport is captured; content can continue below the fold. The
bulk toolbar and direction-selector images are isolated component fixtures,
rather than full navigation screens.

The preview uses labeled fictional records, an in-memory database and an isolated
draft inbox. No customer photos, bank records, purchases or live Firebase data are
included. The bulk/direction component fixtures contain no personal data. Do not
replace these with user transaction images.

All four selected images are from the final build9 set. Earlier `timeline-`,
`library-`, `summary-` and `settings-` captures are intentionally excluded: the
latest refinement changes visible timeline wording and adds Pip companions, so
the historical captures should not be presented as current build9 screens.

Source verification:

- `Launch/NativeRedesignQA/README.md`
- `Launch/PlaytestRefinementQA.md` (671-test passing run)
- `ReadSlipTests/NativeLibraryPresentationTests.swift`
- `ReadSlip/Views/LibraryExperience.swift`
- `ReadSlip/Views/BatchDraftSelectionToolbar.swift`
- `ReadSlip/Views/SlipDirectionSelector.swift`
