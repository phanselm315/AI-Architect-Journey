# Resume Builder Skill

**Status:** ✅ Done  
**Started:** May 2, 2026  

## What This Is

Claude skill trained iteratively over many real resume tailoring sessions. Provide a job
description, it produces a tailored version of a formatted master resume — pulling from
pre-approved language developed across past versions. Built after doing enough manual
tailoring to recognize the pattern was worth formalizing.

## Architecture

- **Format:** Claude skill (structured system prompt deployed in Cowork)
- **Inputs:** Target job description + master resume
- **Processing:**
  - Maps job requirements to relevant experience
  - Selects and adapts pre-approved language from past resume versions
  - Applies consistent formatting rules
- **Output:** Tailored .docx resume, formatted to spec

**Training approach:** Iterative — each real use session refined the language bank and
edge-case handling. The skill improved through actual use, not hypothetical testing.

## Key Decisions

**Build the skill after enough manual reps to know what it needs.** The first several
resume tailoring sessions were done manually. That experience revealed exactly where the
friction was, what language patterns repeated, and where judgment calls were needed.
Building the skill from that foundation produced a much better prompt than starting from
scratch.

**Pre-approved language bank over open-ended generation.** Resumes require specific,
defensible language — not creative writing. The skill works from a library of phrases
already validated for accuracy and tone, adapting and selecting rather than generating
from scratch. More reliable output, less review time.

**Skill over script.** This is a judgment-heavy task — mapping job requirements to
experience requires reading context, not just pattern matching. A Claude skill handles
the reasoning; a script couldn't.

## Lessons Learned

The best time to formalize a workflow into a skill is after you've done it manually
enough times to recognize the pattern. Building from real experience produces constraints
and guardrails that you wouldn't have anticipated up front.

Iterative training on real use cases compounds quickly. A skill that handles 70% of cases
well after the first version handles 95% after ten real uses, if you update it after each one.

---

*Part of [Finance Engineering](../../README.md)*
