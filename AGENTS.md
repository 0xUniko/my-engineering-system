# AGENTS.md

- Optimize for local static reasoning: keep control flow, state transitions, effects, and call targets inferable from nearby code.
- Use explicit, concrete data structures and types that encode exactly the valid states and alternatives; handle alternatives with explicit case analysis.
- Use polymorphism only for genuine parametric genericity; do not use inheritance or runtime dispatch.
- Avoid explicit loops unless explicitly allowed; use idiomatic functional combinators such as `map`, `filter`, `fold`, and language-specific equivalents.
- Except where required by third-party APIs, mutable state may exist only as state threaded through `fold`.
