# Business Prompt Library

**Status:** ✅ Done  
**Started:** Mar 2026  

## What This Is

Six production-grade Claude skills covering CFO/CCO advisory, SEC compliance, investment
company accounting, community email drafting, website copy, and resume building. All
deployed and in active use in Cowork.

## Architecture

Each skill is a structured system prompt with:
- A defined role and operating context
- Hard rules the model cannot override
- Reference file pointers for persistent context
- Session start/close protocols for stateful work
- Output format standards

**Skills built:**
- `pch-advisory` — CFO/COO advisory operations for Wacker Advisors LLC
- `regpartner` — SEC private fund compliance (Form ADV, Form PF, Marketing Rule, Custody Rule)
- `invcogaap` — ASC 946 investment company accounting
- `sbgc-email` — Community email drafting with strict brand voice enforcement
- `website-copy` — Wacker Advisors public-facing content
- `resume-builder` — Tailored resume generation from job descriptions

## Key Decisions

**Hard rules over soft instructions.** Early prompts used language like "try to" and
"generally." Production skills use "never," "always," and explicit flags for when the
model must stop and ask. The difference in output consistency is significant.

**Context files over long prompts.** Each skill reads external files at session start
rather than embedding all context in the prompt itself. This keeps prompts maintainable
and makes updates a file edit rather than a prompt rewrite.

**Separate skills per domain.** A single "do everything" prompt produces mediocre results
across all domains. A tightly scoped skill with deep context on one domain produces
expert-level output. Scope traded for quality.

## Lessons Learned

A well-structured system prompt with hard rules and rich context is 10x more useful than
a generic prompt. This is the same principle that makes good software architecture: the
constraint creates the capability.

The investment in building these skills upfront compounds across every session. Work that
used to take an hour of back-and-forth now takes five minutes because the context is
already loaded.

---

*Part of [Finance Engineering](../../README.md)*
