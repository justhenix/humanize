---
name: humanize
description: Write or revise natural, audience-aware language across general prose, chat, email, UI microcopy, product copy, marketing, technical documentation, READMEs, code comments, docstrings, CLI help, logs, error messages, and developer-facing text. Use when wording feels robotic, generic, stiff, translated, overly corporate, vague, or inconsistent. Do not use as the primary skill for papers or academic research writing; use acawrite instead.
---

# Humanize

## Scope

Use this skill for general-purpose language, including:

- Conversation and assistant responses.
- Emails, messages, announcements, and proposals.
- UI labels, buttons, forms, helper text, empty states, onboarding, notifications, and errors.
- Product, landing-page, marketing, and support copy.
- Technical documentation, READMEs, tutorials, and API guidance.
- Code comments, docstrings, identifiers, CLI help, logs, and exceptions.
- Editing and translation that must sound native rather than literal.

Use `$acawrite` as the primary skill for papers, theses, literature reviews, research proposals, scholarly citations, and other academic work. When a task combines research and public communication, apply `$acawrite` to evidence and `$humanize` to delivery.

## Core Standard

Make the text sound like a competent person wrote it for a specific reader and situation. Preserve meaning, facts, constraints, and domain accuracy.

Do not:

- Add personality that conflicts with the requested voice.
- Invent facts, proof, urgency, testimonials, or product capability.
- Replace precise technical language with casual but inaccurate wording.
- Change code behavior, placeholders, localization keys, variables, or commands.
- Flatten every voice into the same conversational style.

## Workflow

### 1. Identify the Communication Contract

Determine:

- Audience.
- Medium.
- User intent.
- Desired action.
- Voice and formality.
- Language and locale.
- Length or character limits.
- Terms that must remain unchanged.
- Accessibility and localization constraints.

Infer low-risk details when obvious. Ask only when a missing choice would materially alter the result.

### 2. Find Robotic Signals

Look for:

- Generic assistant openers and closers.
- Empty enthusiasm or corporate politeness.
- Repeated sentence patterns.
- Vague nouns and inflated verbs.
- Literal translation.
- Unnecessary summaries.
- Unsupported superlatives.
- Too many transitions.
- Long labels and passive instructions.
- Comments that restate code.
- Errors that report failure without recovery.

Fix the communication problem, not a word blacklist.

### 3. Rewrite Around the Reader

Lead with the information or action the reader needs. Prefer concrete nouns, active verbs, and specific outcomes.

Vary sentence length naturally. Keep short text short. Preserve useful nuance in longer text.

Choose the smallest amount of personality that fits the context. A payment failure, a code exception, and a campaign headline should not share the same voice.

### 4. Verify Meaning

Compare the revision with the source:

- Facts and quantities remain unchanged.
- Scope and certainty remain unchanged.
- Required terms remain present.
- Links, tokens, and placeholders remain intact.
- Instructions still lead to the correct action.
- Code and command semantics remain unchanged.

Call out any ambiguity that cannot be resolved safely.

## Anti-AI Slop Rules (2026 Standard)

### 1. English Cliché & "AI Tell" Blacklist

Forbidden high-probability AI filler words and phrases:
- **Verbs**: `delve`, `leverage`, `utilize`, `navigate` (metaphorical), `elucidate`, `facilitate`, `commence`, `foster`, `harness`, `spearhead`.
- **Adjectives**: `robust`, `seamless`, `cutting-edge`, `game-changing`, `crucial`, `pivotal`, `paramount`, `myriad`, `tapestry`, `unparalleled`.
- **Filler Phrases**: `in today's digital age`, `it's worth noting`, `needless to say`, `in conclusion`, `furthermore`, `moreover`, `unlock new potential`, `plays a crucial role`, `testament to`.

### 2. Indonesian Cliché & Paired Construction Blacklist

Forbidden Indonesian AI clichés:
- **Paired Constructions**: `bukan hanya X, tetapi juga Y` (and `tidak hanya X, namun juga Y`).
- **Literal Metaphors**: `menjelajahi` (when `membahas` or `mempelajari` is intended), `melalui lensa`, `di era digital saat ini`, `di dunia yang serba cepat ini`.
- **Filler Openers/Closers**: `tentu saja`, `berikut adalah`, `kesimpulannya`, `dapat dikatakan bahwa`, `tidak dapat dipungkiri bahwa`.

### 3. Rhythm and Texture (Avoid Uniform AI Cadence)

- **Varied Lengths**: Mix short, punchy 3-8 word sentences with medium explanatory ones. AI defaults to uniform, mid-length sentences—human writing has texture.
- **First Sentence Rule**: Write or start intros directly. Never use generated filler openings.
- **Read-Aloud Test**: Read output aloud. If a sentence stumbles or sounds robotic to speak, rewrite it.
- **Concrete Experience Anchor**: Anchor claims in concrete context, real numbers, or specific outcomes rather than generic assertions.

## General Prose

- Start directly. Avoid `Certainly`, `Here is`, `Let's dive in`, `Tentu saja`, `Berikut adalah`, and similar filler.
- End on the actual point. Avoid generic support closers.
- Prefer specific action verbs over inflated defaults.
- Avoid rigid `not only X, but also Y` constructions and their translations.
- Avoid redundant conclusions beginning with `Overall`, `In summary`, `Intinya`, or `Kesimpulannya`.
- Do not use em dashes (`—`) or double hyphens (`--`) in UI copy or concise documentation; use colons, parentheses, or inline spacing.
- Prefer active voice, but keep passive voice when the actor is unknown or irrelevant.
- Preserve intentional humor, warmth, bluntness, or restraint.

Do not remove a term solely because it appears on an overused-word list. Use it when it is the clearest accurate choice.

## UI Microcopy

### Labels and Actions

- Name actions with verbs: `Save draft`, `Invite member`, `Retry`.
- Use labels that describe the destination or result.
- Keep terminology consistent across screens.
- Avoid clever wording where clarity matters.
- Respect character limits and layout context.

### Forms

- Make labels self-contained.
- Use helper text for format or consequence, not repeated labels.
- Put examples in helper text rather than relying on placeholders.
- Explain why sensitive information is requested.
- Match validation messages to the field and recovery action.

### Errors

Include the useful parts:

1. What happened.
2. What the user can do.
3. What data or progress was preserved.
4. A support path when self-recovery is impossible.

Avoid blame, internal codes without explanation, and false reassurance. Keep technical detail for logs or expandable diagnostics.

### Empty and Success States

- Explain why the state is empty when helpful.
- Offer one clear next action.
- Confirm the result without celebration that slows the user down.
- Do not use success copy when the operation is still processing.

### Accessibility and Localization

- Do not convey meaning through color alone.
- Write descriptive link and button text.
- Avoid idioms that translate poorly.
- Keep nouns and verbs separable when the interface uses localization variables.
- Preserve placeholders exactly, including `{name}`, `%s`, `{{count}}`, and ICU syntax.

## Technical Writing

### Documentation

- Begin with the user outcome and prerequisites.
- Use steps for sequences and prose for explanation.
- Keep examples executable and consistent with the text.
- State defaults, side effects, failure modes, and version constraints.
- Avoid calling a task `simple` or `easy`.

### Code Comments

- Explain why, constraints, invariants, tradeoffs, or non-obvious behavior.
- Do not narrate visible syntax.
- Keep task-marker comments actionable and scoped.
- Preserve issue references and ownership conventions.

Bad:

```text
Increment i by one.
```

Better:

```text
Skip the header row before processing records.
```

### Docstrings and API Text

- Describe the contract, inputs, outputs, exceptions, side effects, and edge cases.
- Match the project's documentation convention.
- Keep type information out of prose when the signature already states it, unless clarification is needed.

### CLI, Logs, and Exceptions

- State the failed operation.
- Name the relevant resource without exposing secrets.
- Give a corrective action when known.
- Keep stable machine-readable codes if callers rely on them.
- Avoid punctuation and jokes that make repeated logs noisy.

Preserve commands, flags, paths, identifiers, and code formatting exactly unless the task includes changing them.

## Product and Marketing Copy

- Lead with a concrete user outcome.
- Support claims with available proof.
- Replace generic superlatives with differentiators.
- Keep calls to action specific to the next step.
- Match the user's stage of awareness.
- Avoid manufactured scarcity, deceptive urgency, and unverifiable comparisons.

Do not make ordinary functionality sound revolutionary.

## Translation and Bilingual Text

Translate intent, register, and context, not word order. Preserve names, terms, placeholders, and technical meaning.

For Indonesian:

- Prefer natural Indonesian sentence order.
- Avoid literal phrases such as `menjelajahi topik` or `melalui lensa` when `membahas` or `berdasarkan perspektif` is clearer.
- Use `menghadapi`, `bidang`, `perkembangan`, `meningkatkan`, or `utama` when they express the intended meaning better than common AI defaults.
- Avoid `bukan hanya X, tetapi juga Y` and equivalent paired constructions.
- Use established technical terms rather than awkward translations.

For English, avoid corporate filler, stacked nouns, and abstract verbs when a direct alternative exists.

## Output Behavior

Return the rewritten artifact first. Add notes only when they help the user understand:

- A material meaning change.
- A terminology decision.
- A character-limit tradeoff.
- An ambiguity.
- A preserved technical constraint.

For multiple UI strings, use a compact table with context, original, revision, and rationale when comparison matters. For code, provide the smallest valid patch or replacement.

## Final Check

Before delivering:

- The reader, medium, and action are clear.
- The voice matches the context.
- The wording is concrete and natural.
- No facts or capabilities were invented.
- Certainty and scope remain intact.
- UI text is concise, actionable, and accessible.
- Technical text is accurate and useful.
- Code tokens and placeholders remain unchanged.
- Repetition, filler, and unnecessary hype are removed.
- The output follows the requested language and constraints.
