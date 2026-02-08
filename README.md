# joke-absurdity-scorer

A scalar function that evaluates the absurdity level of jokes, returning a score from 0 (completely grounded in reality) to 1 (pure absurdism).

## Overview

This function measures how completely a joke departs from rational coherence across five distinct dimensions of absurdity. It distinguishes quality absurdist humor (Monty Python, Kafka, surrealism) from lazy randomness, and recognizes absurdity as a legitimate comedic mode with its own internal logic.

## Input

The function accepts a single `joke` field that can be:
- **Text**: One-liners, absurdist stories, nonsense verse, surreal narratives
- **Image**: Surreal memes, dadaist comics, impossible visual juxtapositions
- **Video**: Absurdist sketches, surreal TikToks, anti-comedy performances

## Dimensions Evaluated

### 1. Reality Rupture
How completely the joke breaks from physical, logical, or social reality. Ranges from "Grounded" (everything could happen) to "Dissolved" (reality is meaningless).

### 2. Semantic Dissolution
How thoroughly the joke undermines semantic coherence. Ranges from "Stable" (words mean what they mean) to "Void" (pure noise).

### 3. Tonal Commitment
How seriously the joke presents its absurd content. Quality absurdism treats nonsense with a straight face, while "random" humor winks at itself. Ranges from "Uncommitted" to "Transcendently Committed."

### 4. Internal Dream Logic
Whether the joke's absurdity follows its own internal rules. Paradoxically, great absurdism maintains consistency within impossibility. Ranges from "Chaotic" to "Rigorous."

### 5. Existential Resonance (Mapped)
Whether the absurdity engages with philosophical themes, evaluated across five existential dimensions:
- **Meaninglessness**: Futility of searching for meaning
- **Alienation**: Disconnection and failure of communication
- **Arbitrary Systems**: Absurdity of bureaucracy and social norms
- **Identity Dissolution**: Instability of selfhood
- **Cosmic Indifference**: Insignificance in an uncaring universe

## Output

A scalar value from 0 to 1:
- **0.0-0.2**: Grounded humor (puns, observational comedy)
- **0.2-0.4**: Mild absurdity (exaggeration, surreal touches)
- **0.4-0.6**: Moderate absurdity (some impossible elements)
- **0.6-0.8**: Strong absurdity (reality unstable, possible existential themes)
- **0.8-1.0**: Pure absurdism (Kafkaesque, transcendent nonsense)

## Example Scores

| Joke Type | Expected Score |
|-----------|---------------|
| "Why did the scarecrow win an award? He was outstanding in his field." | ~0.1 |
| Monty Python fish license sketch | ~0.7 |
| "LOL so random *holds up spork*" | ~0.4 |
| Kafkaesque bureaucracy becoming a concept | ~0.9 |
| Pure semantic nonsense ("The color of sound was Thursday's nephew") | ~0.85 |

## Use Cases

- **Content curation**: Surface surreal content for users who enjoy it
- **Creative feedback**: Help comedians understand their absurdity profile
- **Academic analysis**: Quantify trends in absurdist humor
- **Quality control**: Distinguish intentional absurdism from failed conventional jokes
