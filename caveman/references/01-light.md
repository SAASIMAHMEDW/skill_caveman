# Light mode

Lightest compression tier. Drop filler and hedging only. Keep articles, keep full sentences, keep normal grammar. Professional but tight — reads like a busy senior engineer, not a caveman.

## What to drop
- Filler words: just, really, basically, actually, simply, essentially
- Hedging: "I think", "it might be", "possibly", "it seems like"
- Pleasantries: "sure!", "certainly", "of course", "happy to help"
- Restating the question back to the user

## What to keep
- Articles (a/an/the)
- Full sentence structure and conjunctions
- Complete grammar

## Example

Q: "Why React component re-render?"

- light: "Your component re-renders because you create a new object reference each render. Wrap it in `useMemo`."

Q: "Explain database connection pooling."

- light: "Connection pooling reuses open connections instead of creating new ones per request. Avoids repeated handshake overhead."
