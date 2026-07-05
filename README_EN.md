# SISFIT Coursepack Skill

An LLM skill for Chinese-speaking body education teachers who want to turn a health topic into a structured, boundary-aware, sellable coursepack outline.

## What It Does

This skill helps teachers organize a topic into a reusable coursepack structure, including:

- positioning
- suitable and unsuitable audiences
- course goals
- course structure and flow
- classroom cue directions
- boundary-safe wording
- preheat content directions
- sales page structure

Its job is not to provide medical judgment. Its job is to support health-education planning, course structuring, and productized communication.

## Best Use Cases

- offline themed classes
- online class or livestream planning
- Xiaohongshu / Moments / WeChat preheat content
- sales-page structure for a coursepack
- reducing risky or over-medicalized wording in health education content

## Not For

- medical diagnosis
- disease judgment
- definitive pain-cause claims
- treatment advice
- rehabilitation prescriptions
- individualized medical advice

If the input involves trauma, swelling, numbness, fever, night pain, or obvious movement restriction, the skill should first advise offline medical evaluation or consultation with a qualified professional.

## Installation

Place this directory under:

```text
~/.trae/skills/sisfit-coursepack/
```

Minimum expected files:

- `SKILL.md`
- `README.md`
- `README_EN.md`
- `examples.json`
- `boundary_checklist.md`
- `xiaohongshu_post.md`

## When To Invoke It

Use this skill when the user wants to:

- generate a body-topic coursepack outline
- turn a theme into a sellable course structure
- draft flow, cueing, and wording boundaries for a class
- create Xiaohongshu preheat directions or a sales page skeleton

Example requests:

- "Help me create a coursepack outline for this body topic."
- "Turn this topic into a 60-minute offline class structure."
- "Draft classroom cueing and a sales page structure for this theme."

## Input Template

```text
Teacher type:
Target audience:
Body topic:
Course length:
Use case:
Core idea I want to communicate:
Questions students often ask:
Existing movement or practice materials:
Any special population involved:
```

## Output Structure

The skill is designed to output 12 sections:

1. Topic positioning
2. Suitable audience
3. Unsuitable audience
4. Common user language
5. Course goals
6. Course structure
7. Course flow
8. Classroom cue directions
9. Boundary wording checklist
10. Preheat content directions
11. Sales page structure
12. Risk reminder

## Example Coverage

See [examples.json](./examples.json). The current example set covers:

- standard course structures
- preheat content for social platforms
- sales-oriented outputs
- risk-boundary routing for high-risk inputs
- topics across breathing, sleep, postpartum, neck/shoulder, low back, hips, feet, and standing fatigue

## Files

- `SKILL.md`: core prompt and behavioral rules
- `README.md`: Chinese overview
- `README_EN.md`: English overview
- `examples.json`: example inputs and expected use cases
- `boundary_checklist.md`: safety wording checklist
- `xiaohongshu_post.md`: posting copy draft

## Current Status

Repository packaging version: `v0.1.2`  
Core `SKILL.md` prompt version: `v0.1.0`

This is still a public draft suitable for:

- GitHub sharing
- internal versioning
- small-scale testing and iteration

See [CHANGELOG.md](./CHANGELOG.md) for release notes.

## License

This repository is licensed under the [MIT License](./LICENSE).
