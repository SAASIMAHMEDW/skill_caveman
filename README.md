# caveman

Ultra-compressed communication mode for AI coding agents. Cuts response length while keeping full technical accuracy.

Works with any agent supporting the [Agent Skills](https://agentskills.io/specification) standard — Claude Code, Claude (claude.ai), Cursor, GitHub Copilot, Codex, Gemini CLI, and others that read `SKILL.md`.

## Attribution

This is a derivative of the original **[caveman](https://github.com/juliusbrussee/caveman)** skill by **juliusbrussee**. All credit for the original concept and design goes there.

Changes made in this fork:
- Renamed modes for clarity: `lite/full/ultra/wenyan-lite/wenyan-full/wenyan-ultra` → `light/caveman/ultra/sage-light/sage/sage-ultra`
- Fixed a bug where the highest classical-compression tier (`wenyan-ultra` → now `sage-ultra`) emitted actual Chinese characters instead of English. Sage tiers now borrow classical Chinese *grammar structure* (verb-first, subject drop, arrow-causality) but always output English words.
- Restructured into a proper skill package: `SKILL.md` now holds only routing logic; full mode detail moved to `references/` for progressive disclosure (less context loaded until a mode is actually used)
- Added `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `CHANGELOG.md`, `LICENSE`

## Install

```bash
# via GitHub
npx skills add <your-org>/caveman

# local
npx skills add ./caveman
```

## Modes

| Mode | What it does |
|---|---|
| `light` | Drop filler/hedging only, full sentences |
| `caveman` (default) | Drop articles, fragments ok, classic terse style |
| `ultra` | Abbreviate prose words, arrows for causality |
| `sage-light` | Classical grammar structure, softened, English words |
| `sage` | Max classical terseness, English words |
| `sage-ultra` | Most compressed sage tier, English words |

Switch mode mid-conversation: `/caveman ultra`, `/caveman sage`, etc.
Turn off: say "stop caveman" or "normal mode".

## Structure

```
caveman/
├── SKILL.md              — routing logic, mode table, core rules
├── references/
│   ├── 01-light.md
│   ├── 02-caveman.md
│   ├── 03-ultra.md
│   ├── 04-sage.md
│   └── 05-boundaries.md
├── README.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── CHANGELOG.md
└── LICENSE
```

## License

MIT — see [LICENSE](./LICENSE).
