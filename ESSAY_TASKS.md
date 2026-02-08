# ESSAY_TASKS: Tasks for joke-absurdity-scorer

The following tasks comprise the evaluation pipeline for scoring the absurdity of jokes. Each task corresponds to one of the five dimensions of absurdity defined in ESSAY.md. These tasks are designed to be very distinct from one another, capturing fundamentally different facets of how humor departs from rational coherence.

---

## Task 1: Reality Rupture Evaluation

**Dimension:** Reality Rupture — The Degree of Departure from the Possible

**Purpose:** Assess how completely the joke breaks from physical, logical, or social reality. This is the most fundamental dimension of absurdity, measuring the extent to which a joke presents scenarios that could not occur in the real world.

**Evaluation Criteria:**
- Does the joke present physically impossible scenarios (talking objects, impossible transformations, defiance of physics)?
- Are cause-and-effect relationships severed, inverted, or nonsensical?
- Do characters or entities behave in ways that defy basic logic or psychology?
- Has the setting transformed from recognizable reality into something alien or impossible?

**Response Options (5-point spectrum):**
1. **Grounded** — Everything in the joke could happen in the real world; no impossible elements
2. **Bent** — Reality is stretched through exaggeration or hyperbole, but nothing truly impossible occurs
3. **Fractured** — Some impossible elements exist within an otherwise normal framework
4. **Shattered** — Reality is fundamentally unstable; impossible things are treated as normal
5. **Dissolved** — The very concept of reality has become meaningless; pure impossibility

**Output Mapping:** Grounded=0.0, Bent=0.25, Fractured=0.5, Shattered=0.75, Dissolved=1.0

---

## Task 2: Semantic Dissolution Evaluation

**Dimension:** Semantic Dissolution — The Breakdown of Meaning

**Purpose:** Assess how thoroughly the joke undermines semantic coherence, attacking meaning itself rather than just physical reality. This dimension captures the degree to which words, categories, and communication break down.

**Evaluation Criteria:**
- Do words maintain stable, conventional meanings, or do they drift and mutate?
- Are categorical boundaries respected (nouns remain nouns, concrete things remain concrete)?
- Does the joke employ non sequiturs that resist any coherent interpretation?
- Is there a sense that language itself is being satirized, deconstructed, or rendered meaningless?

**Response Options (5-point spectrum):**
1. **Stable** — Language operates normally; words mean what they conventionally mean
2. **Playful** — Puns and double meanings exploit semantic flexibility, but within coherent bounds
3. **Slippery** — Meanings shift unexpectedly; context fails to anchor interpretation
4. **Dissolving** — Categories collapse; nouns become verbs, concrete becomes abstract, sense becomes nonsense
5. **Void** — Semantic content approaches zero; communication has become pure noise or phonetic play

**Output Mapping:** Stable=0.0, Playful=0.25, Slippery=0.5, Dissolving=0.75, Void=1.0

---

## Task 3: Tonal Commitment Evaluation

**Dimension:** Tonal Commitment — The Seriousness of the Nonsense

**Purpose:** Assess how seriously the joke presents its absurd content. Quality absurdist humor often derives power from treating nonsense with a straight face, while self-conscious "random" humor signals its own silliness. This dimension distinguishes crafted absurdism from lazy randomness.

**Evaluation Criteria:**
- Does the joke wink at its own absurdity, or does it present nonsense deadpan?
- Is there internal consistency in how characters react to impossible situations?
- Do characters treat the absurd as mundane, or do they acknowledge the strangeness?
- Does the work commit to its bizarre premise, or does it break frame to signal "this is silly"?

**Response Options (5-point spectrum):**
1. **Uncommitted** — The joke signals awareness of its own silliness; winking, mugging, or "so random" energy
2. **Semi-committed** — Mostly straight-faced but with occasional acknowledgment of the absurdity
3. **Committed** — Treats the absurd scenario with genuine seriousness throughout
4. **Fully Committed** — The absurdity is presented as utterly mundane; no one notices anything unusual
5. **Transcendently Committed** — The seriousness is so total it loops back to being absurd; the commitment itself is the joke

**Output Mapping:** Uncommitted=0.0, Semi-committed=0.25, Committed=0.5, Fully Committed=0.75, Transcendently Committed=1.0

---

## Task 4: Internal Dream Logic Evaluation

**Dimension:** Internal Dream Logic — Coherence Within Incoherence

**Purpose:** Assess whether the joke's absurdity follows its own internal rules. Paradoxically, the best absurdist humor maintains consistency within its impossible framework—a dream logic that, while not mapping to reality, is predictable within its own terms.

**Evaluation Criteria:**
- Does the joke establish impossible premises and then follow them consistently?
- Is there a sense of inevitability within the absurd framework?
- Do the absurd elements relate to each other in patterned, predictable ways?
- Could you anticipate what would happen next based on the established dream logic?

**Response Options (5-point spectrum):**
1. **Chaotic** — Pure randomness with no internal consistency; elements are arbitrary and disconnected
2. **Sporadic** — Occasional patterns emerge but dissolve quickly; inconsistent logic
3. **Emerging** — A dream logic is partially visible; some absurd elements connect to each other
4. **Consistent** — Clear internal rules govern the absurdity; the impossible is predictable within its own terms
5. **Rigorous** — The absurd framework is more strictly logical than reality itself; impossibility with mathematical precision

**Output Mapping:** Chaotic=0.0, Sporadic=0.25, Emerging=0.5, Consistent=0.75, Rigorous=1.0

---

## Task 5: Existential Resonance Evaluation (MAPPED)

**Dimension:** Existential Resonance — Absurdity as Philosophy

**Purpose:** Assess whether the absurdity transcends mere silliness to engage with profound questions about meaning, existence, and the human condition. This dimension captures the philosophical depth of absurdist humor, from pure entertainment to Kafkaesque illumination.

**Evaluation Criteria:**
- Does the absurdity comment on the human search for meaning in a meaningless universe?
- Does it evoke the feeling of being a conscious being in an indifferent cosmos?
- Does it capture something true about the arbitrary nature of existence, identity, or society?
- Does it provoke uncomfortable recognition alongside laughter—the sense that the joke is "about something"?

**Task Type:** This task uses a MAPPED approach with weighted binary evaluations across multiple existential themes.

**Sub-evaluations:**

### 5a: Meaninglessness Theme
Does the joke engage with the theme of meaninglessness or the futility of searching for meaning?
- **NO** — The joke does not engage with themes of meaninglessness
- **YES** — The joke comments on futility, meaninglessness, or the absurdity of seeking meaning

### 5b: Alienation Theme
Does the joke engage with the theme of alienation, disconnection, or the failure of communication?
- **NO** — The joke does not engage with themes of alienation
- **YES** — The joke captures isolation, disconnection, or the impossibility of being truly understood

### 5c: Arbitrary Systems Theme
Does the joke satirize or illuminate the arbitrary nature of social systems, rules, or conventions?
- **NO** — The joke does not engage with arbitrary systems
- **YES** — The joke exposes the absurdity of bureaucracy, social norms, or human-made structures

### 5d: Identity Dissolution Theme
Does the joke engage with the instability or arbitrariness of identity and selfhood?
- **NO** — The joke does not engage with identity themes
- **YES** — The joke questions who we are, the stability of the self, or the arbitrariness of identity

### 5e: Cosmic Indifference Theme
Does the joke evoke the feeling of existing in an indifferent universe that doesn't care about human concerns?
- **NO** — The joke does not engage with cosmic indifference
- **YES** — The joke captures the feeling of being insignificant in a vast, uncaring cosmos

**Output Mapping:** Each YES response contributes 0.2 to the final score (total possible: 1.0 if all five themes are present, 0.0 if none).

---

## Summary of Task Types

| Task | Dimension | Type | Output Range |
|------|-----------|------|--------------|
| 1 | Reality Rupture | 5-point spectrum | 0.0 - 1.0 |
| 2 | Semantic Dissolution | 5-point spectrum | 0.0 - 1.0 |
| 3 | Tonal Commitment | 5-point spectrum | 0.0 - 1.0 |
| 4 | Internal Dream Logic | 5-point spectrum | 0.0 - 1.0 |
| 5 | Existential Resonance | Mapped (5 binary) | 0.0 - 1.0 |

## Notes on Task Design

- **Distinctiveness:** Each task evaluates a fundamentally different aspect of absurdity. A joke could score high on Reality Rupture but low on Tonal Commitment (winking surrealism), or high on Internal Dream Logic but low on Semantic Dissolution (consistent fantasy with clear language).

- **The Mapped Task:** Task 5 (Existential Resonance) uses a mapped approach with five binary sub-evaluations rather than a single spectrum. This captures the multi-dimensional nature of philosophical depth—a joke might engage with alienation but not cosmic indifference, for example.

- **Independence from Other Scorers:** These dimensions are specifically designed to avoid overlap with existing scorers. Surprise-scorer evaluates expectation subversion; absurdity-scorer evaluates departure from possibility. Cleverness-scorer evaluates intellectual craft; absurdity-scorer evaluates embrace of the irrational.

- **Quality Gradient:** Higher scores do not necessarily mean "better" jokes—they mean "more absurd" jokes. A grounded observational joke scores 0 on absurdity but might be brilliant. This scorer measures intensity of absurdity, not quality of humor.
