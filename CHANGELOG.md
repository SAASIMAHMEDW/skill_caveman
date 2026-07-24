# Changelog

All notable changes to this fork are documented here.

## [1.0.0] — Initial fork release

### Changed
- Renamed all modes for clarity:
  - `lite` → `light`
  - `full` → `caveman` (now the explicit default, matches skill name)
  - `ultra` → `ultra` (unchanged)
  - `wenyan-lite` → `sage-light`
  - `wenyan-full` → `sage`
  - `wenyan-ultra` → `sage-ultra`
- Restructured single-file `SKILL.md` into a full skill package: routing logic and shared rules stay in `SKILL.md`, full per-mode detail and examples moved to `references/` for progressive disclosure.

### Fixed
- **Critical:** `wenyan-ultra` (now `sage-ultra`) previously emitted actual Chinese characters in responses instead of English. Root cause: mode description conflated "classical Chinese compression structure" with "respond in Chinese." Fixed by explicitly separating the two — sage tiers now use classical grammar patterns (verb-first ordering, subject omission, arrow-causality) while requiring English-only output, documented as a hard rule in `references/04-sage.md`.

### Added
- `README.md` with attribution, install instructions, mode table
- `CONTRIBUTING.md` for extending modes/checklists
- `CODE_OF_CONDUCT.md` (Contributor Covenant 2.1)
- `SECURITY.md` — scope note (Markdown-only, no execution surface) and reporting process
- `LICENSE` (MIT)

### Credits
Original concept and design: [juliusbrussee/caveman](https://github.com/juliusbrussee/caveman).
