# Contributing

This is a fork of [juliusbrussee/caveman](https://github.com/juliusbrussee/caveman). Consider contributing upstream first if your change is general-purpose; contribute here if it's specific to this fork's mode names or the sage English-only fix.

## Adding a new mode / level

1. Add a row to the level table in `SKILL.md`.
2. Create a new file under `references/` following the existing naming pattern (`0N-name.md`).
3. Include in the reference file:
   - What to drop / add vs. the tier below it
   - What must stay unchanged (code, error strings, technical terms)
   - At least 2 worked examples
4. Update `README.md`'s mode table.
5. Add a `CHANGELOG.md` entry.

## Editing an existing checklist/rule

- Keep the "core rules" in `SKILL.md` minimal — only rules that apply to every level belong there. Tier-specific detail belongs in `references/`.
- Never remove the sage English-only rule or weaken its wording — this fixes a real regression (see CHANGELOG v1.0.0).
- Test any wording change against the worked examples in the relevant reference file; update examples if behavior changes.

## Style for reference files

- Short sections: "What to drop", "What to keep", "Example"
- Examples should be realistic dev questions, not abstract
- No filler in the docs themselves — this skill teaches terseness, its own docs should model it where reasonable (though full clarity always wins in reference docs)

## Reporting issues

Open a GitHub issue describing: which mode, what input, expected vs actual output.
