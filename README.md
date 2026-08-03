# Humanize Skill

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Skills CLI](https://img.shields.io/badge/skills.sh-humanize-blue.svg)](https://skills.sh)

Stop AI from using bizarre writing patterns. Write and revise natural, audience-aware language across prose, UI microcopy, product copy, marketing, technical documentation, code comments, docstrings, CLI help, logs, and bilingual text (English & Indonesian).

---

## Quickstart & Installation

Install into your AI Agent workspace or CLI environment (Claude Code, Cursor, Antigravity, Kiro, Codex, etc.) using `skills`:

```bash
npx skills add https://github.com/justhenix/humanize --skill humanize
```

---

## Key Features

### 1. English Cliché & "AI Tell" Blacklist
Explicit prohibition of overused AI verbs (`delve`, `leverage`, `utilize`, `navigate`, `elucidate`, `facilitate`), adjectives (`robust`, `seamless`, `cutting-edge`, `crucial`, `pivotal`, `myriad`, `tapestry`), and filler phrases (`in today's digital age`, `it's worth noting`, `needless to say`, `unlock new potential`).

### 2. Indonesian Cliché & Paired Construction Blacklist
Prohibition of rigid constructions (`bukan hanya X, tetapi juga Y`), literal AI metaphors (`menjelajahi` when `membahas` is intended, `melalui lensa`), and filler openers (`tentu saja`, `berikut adalah`, `kesimpulannya`).

### 3. Texture Over Smooth Cadence
Eliminates smooth, uniform AI sentence lengths. Mixes short, punchy 3–8 word sentences with medium explanatory ones to mirror genuine human rhythm.

### 4. Concrete Experience Anchor & Read-Aloud Test
Requires grounding claims in real context, concrete numbers, or verifiable outcomes. Includes a mandatory read-aloud test and if a sentence feels awkward to speak, it gets rewritten.

---

## Scope

- **Prose & Chat**: Direct openings, zero filler intros/closers, zero generic support sign-offs.
- **UI Microcopy**: Verb-first action labels, actionable error messages with recovery paths, self-contained form labels.
- **Technical Writing**: Code comments explaining *why* instead of narrating syntax, accurate docstrings, clean CLI/exception logs.
- **Bilingual & Localization**: Natural Indonesian sentence order and idiomatic English without corporate fluff.

---

## License

[MIT](LICENSE) © Henix
