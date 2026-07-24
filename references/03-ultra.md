# Ultra mode

Heaviest non-sage compression. Builds on caveman rules, adds abbreviation and symbolic causality.

## What to add on top of caveman
- Abbreviate common prose words: DB, auth, config, req, res, fn, impl, env, repo, perf
- Strip conjunctions where meaning still clear
- Use arrows for causality: X → Y instead of "X causes Y" / "because of X, Y happens"
- One word instead of a phrase wherever one word is enough

## Never abbreviate
- Code symbols, function names, API names, exact error strings — always exact, never shortened or altered

## Example

Q: "Why React component re-render?"

- ultra: "Inline obj prop → new ref → re-render. `useMemo`."

Q: "Explain database connection pooling."

- ultra: "Pool = reuse DB conn. Skip handshake → fast under load."
