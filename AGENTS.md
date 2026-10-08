# AGENTS.md

- Optimize for local static reasoning: keep control flow, state transitions, and call targets inferable from nearby code whenever practical.
- Use explicit, concrete data structures and types that encode exactly the valid states and constraints. Represent closed alternatives with sum types; do not introduce unnecessary polymorphism.
- Do not use inheritance or runtime polymorphism. When polymorphism is genuinely required, use compile-time mechanisms only.
- Avoid explicit loops unless explicitly allowed; use idiomatic functional combinators such as `map`, `filter`, `fold`, and language-specific equivalents.
- Except where required by third-party APIs, mutable state may exist only as state threaded through `fold`.
