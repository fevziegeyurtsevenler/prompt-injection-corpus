# Contributing to prompt-injection-corpus

Contributions are welcome — especially **non-English techniques** and **stronger
defenses**. This is a defenders' resource; every entry must help someone harden a
system.

## Rules

1. **Every technique ships with its defense.** No exception. An entry without a
   defense will not be merged.
2. **Authorized/defensive framing only.** Nothing targeting a real, non-consenting
   system. See [ETHICS.md](ETHICS.md).
3. Follow the entry shape: *technique name → example → expected bad outcome →
   defense*, and map to OWASP LLM Top 10 / MITRE ATLAS where possible.
4. Keep examples illustrative, not weaponized end-to-end kill chains.

## Especially wanted

- Additional languages (the multilingual gap is the whole point).
- Turkish morphological / code-switch variants.
- Defenses that are testable (a detection rule, a guardrail config).

Open a PR; describe the category and why the technique matters.
