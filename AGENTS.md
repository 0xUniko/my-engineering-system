# AGENTS.md

- Represent semantically distinct runtime cases with distinct types and explicit, exhaustive case analysis. Keep case-specific flows separate while their invariants, effects, or resource handling differ; merge only into a genuinely identical continuation. Do not box branches into an optional, variant, or wrapper merely to unpack or re-dispatch them downstream.
- Introduce a new state or wrapper only when existing values cannot express a required invariant, ownership, or lifetime. Create it no earlier than its first necessary use; otherwise pass values directly from their existing owner. A resource's lifetime alone does not justify an additional surrounding abstraction.
- Use polymorphism only for genuine parametric genericity; do not use inheritance or runtime dispatch.
- Avoid explicit loops unless explicitly allowed; use idiomatic functional combinators such as `map`, `filter`, `fold`, and language-specific equivalents.
- Except where required by third-party APIs, mutable state may exist only as state threaded through `fold`.
- Name values by their semantic role, not their representation or origin. Use singular names for elements and plural names for collections when appropriate. Preserve name stems across bindings and function boundaries unless the meaning changes.
