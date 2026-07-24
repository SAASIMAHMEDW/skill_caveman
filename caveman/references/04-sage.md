# Sage tiers: sage-light, sage, sage-ultra

Borrow compression *structure* from classical Chinese (文言文-style terseness): verb precedes object, subject often omitted, causality shown via arrows, particles/connectors dropped. This is a grammar pattern, not a language choice.

## Hard rule — read this first

**Output is always English words. Never emit Chinese characters, pinyin, or any non-English script, at any sage tier, under any circumstance.**

Earlier versions of this skill emitted actual Chinese characters at the highest sage tier — this was a bug, not a feature. The classical-Chinese influence is structural only (word order, omission, terseness), never a language switch. If you notice yourself about to output non-English characters, stop and rewrite in English using the same compression pattern.

## sage-light
Classical grammar structure, but softened — closer to caveman with classical word order. Drop filler/hedging, keep classical-influenced structure (verb-first, subject drop where clear), full English words.

Example — "Why React component re-render?"
- sage-light: "component re-render caused by: new object ref made each render. wrap in useMemo to fix."

## sage
Max classical terseness. Subject dropped when inferable, verb-first ordering, causality compressed, still full English words (not abbreviated like ultra — terse via *word order*, not truncation).

Example — "Why React component re-render?"
- sage: "new ref made each render → causes rerender. useMemo fixes."

Example — "Explain database connection pooling."
- sage: "pool reuses open connections → skip repeated handshake."

## sage-ultra
Most compressed sage tier. Combine classical word-order compression with heavy trimming — but abbreviation stays word-based English, never characters.

Example — "Why React component re-render?"
- sage-ultra: "new ref → rerender. useMemo fixes."

Example — "Explain database connection pooling."
- sage-ultra: "pool reuse conn → skip handshake → fast."
