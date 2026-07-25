<h1 align="center">prompt-injection-corpus</h1>

<p align="center">
  <b>A multilingual (English + Turkish) corpus of prompt-injection & jailbreak
  techniques — for defenders.</b><br>
  Categorized techniques with example payloads, expected failure modes, and the
  defense for each — mapped to OWASP LLM Top 10 &amp; MITRE ATLAS.
</p>

<p align="center">
  <a href="LICENSE"><img alt="License: CC BY 4.0" src="https://img.shields.io/badge/data-CC--BY--4.0-blue.svg"></a>
  <img alt="Languages" src="https://img.shields.io/badge/lang-EN%20%2B%20TR-informational">
  <img alt="Categories" src="https://img.shields.io/badge/categories-5-brightgreen.svg">
</p>

---

> ⚠️ **Authorized, defensive use only.** This corpus exists to help you **test and
> harden systems you own or are explicitly authorized to assess** — building
> detections, red-teaming your own LLM apps, training classifiers. Using these
> techniques against systems you do not control is prohibited and, in many
> jurisdictions, illegal. See [ETHICS.md](ETHICS.md).

Most public jailbreak/injection collections are **English-only** — so non-English
attacks slip past filters that were only ever tested in English. This corpus is
**multilingual first**, with a dedicated Turkish morphological/code-switch section,
because that gap is exactly where real-world filters fail.

## What's inside (`techniques/`)

| File | Category | Frameworks |
|---|---|---|
| `01-direct-injection.md` | Direct prompt injection | OWASP LLM01 |
| `02-indirect-injection.md` | Indirect / RAG injection (via documents, tools, web) | OWASP LLM01 · ATLAS |
| `03-jailbreak-persona.md` | Jailbreak & persona manipulation (DAN-style, "developer mode") | OWASP LLM01 |
| `04-data-exfiltration.md` | System-prompt leak & data exfiltration | OWASP LLM02 / LLM06 |
| `05-turkish-morphological.md` | Turkish morphological & code-switch bypass | OWASP LLM01 |

Each entry follows the same shape: **technique → example → expected bad outcome →
defense.** The point is not the payload; it's the *defense* next to it.

## How to use it (defensively)

- **Test your own app:** feed the examples through your LLM app and confirm your
  guardrails hold.
- **Pair it with tooling:** use it alongside [`uncloak`](https://github.com/fevziegeyurtsevenler/uncloak),
  [garak](https://github.com/NVIDIA/garak) or [promptfoo](https://github.com/promptfoo/promptfoo).
- **Build detections:** use the labeled examples to train or evaluate a classifier.

## Related

- [`llm-security-skills`](https://github.com/fevziegeyurtsevenler/llm-security-skills) — Agent Skills that use this corpus to test apps.
- [`skills-in-the-wild`](https://github.com/fevziegeyurtsevenler/skills-in-the-wild) — open audit of real agent extensions.
- [verazuo/jailbreak_llms](https://github.com/verazuo/jailbreak_llms), [awesome-agent-supply-chain-security](https://github.com/fevziegeyurtsevenler/awesome-agent-supply-chain-security).

## Contributing

New techniques (especially non-English) and stronger defenses are welcome — every
entry **must** ship with its defense. See [CONTRIBUTING.md](CONTRIBUTING.md). Do not
submit anything targeting a real, non-consenting system.

## License

Corpus text: [CC BY 4.0](LICENSE). Attribution: *Fevzi Ege Yurtsevenler / AltaySec*.
