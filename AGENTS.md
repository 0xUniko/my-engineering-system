# AGENTS.md

- Keep control flow traceable and state changes localizable.
- Make data structures explicit.
- Encode possibilities and constraints in types when practical.
- Prefer code whose meaning is clear from its local context.
- Do not use loops unless explicitly allowed; prefer `map/transform(c++)`, `fold`, etc.
- Do not use mutable global state.
- Do not use inheritance or runtime polymorphism (e.g. factory-based dispatch); use compile-time polymorphism only, such as type classes.
