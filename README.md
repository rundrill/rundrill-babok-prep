# RunDrill BABOK Prep

Your personal **business-analysis coach** inside your AI agent — prep for the IIBA certification ladder
(**ECBA → CCBA → CBAP**) the way the job actually demands it: by **judging scenarios** and **reviewing
real BA artifacts**, not by memorising definitions or watching the AI write your requirements. Short
targeted drills, an honest picture of your tier, and mistake memory that resurfaces what you got
wrong. Your tier and progress live on the RunDrill MCP server (`mcp.rundrill.com`), synced across
machines — not in a local file.

**Why this course is different.** Business analysis has no compiler: a requirement, a user story, a
stakeholder map doesn't "run", so the skill that matters is *judgment on an artifact*. When an AI can
draft any requirement on demand, the real risk is the *illusion of competence* — accepting one that
reads fine and is quietly wrong: a solution stated as a requirement, a passive-voice requirement that
hides who acts, an untestable "user-friendly", a MoSCoW list where everything is a Must, a stakeholder
list missing the obvious party. Every drill is **blended** — an exam-style scenario judgment paired
with producing a real artifact — and the **signature drill hands you a plausible BA artifact with a
planted defect and asks you to find it, like a peer review.** Plus mock-elicitation role-plays (the AI
plays a stakeholder) and timed cumulative mock exams.

The course is grounded in *BABOK Guide v3* and the current IIBA exam blueprints. It climbs three
tiers — **ECBA** (speak the standard: BACCM, the requirements life cycle, the six knowledge areas) →
**CCBA** (elicit, model, specify: the working toolkit and the bulk of the 50 techniques) → **CBAP**
(shape and justify enterprise change: strategy analysis, solution evaluation, planning, perspectives).
An optional **practitioner** track adds beyond-BABOK job skills: BPMN/UML/DMN, wireframing, Jira/ADO,
SQL & data profiling, API literacy, facilitation, agile ceremonies, and exec readouts.

**Learn in your language.** The IIBA exam is in English, but you don't have to study only in English:
set your native language and the coach explains in it while giving every BABOK term as *native
(English original)* — so you reason naturally and still recognise the official terms on the exam.

## One plugin, three hosts

The coaching skill (`skills/babok-prep-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its
own manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

The MCP endpoint is `https://mcp.rundrill.com/skills/babok` — the skills-course host, passing
`subject: "babok"`. The server routes on the `/skills` segment and ignores the course name; the name
makes BABOK register as its own MCP server in your agent. On first use the host opens a browser tab for
the OAuth handshake, then closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/rundrill
  /plugin install rundrill-babok-prep@rundrill
  ```
  Then run `/babok-prep-coach`.
- **OpenAI Codex** — `codex plugin marketplace add rundrill/rundrill`, then install `rundrill-babok-prep`.
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-babok-prep/`
  (global) or `<workspace>/.agents/plugins/rundrill-babok-prep/` (workspace-scoped).

## A note on BABOK®

This is an independent study aid for learning business analysis and preparing for IIBA® exams. It is
**not** affiliated with or endorsed by IIBA®. *BABOK®*, *ECBA®*, *CCBA®*, and *CBAP®* are trademarks
of the International Institute of Business Analysis. The course teaches the publicly documented
structure and concepts of the discipline in our own words; it does not reproduce the BABOK® Guide.

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE). You may view, run, and share this
plugin unchanged, non-commercially, with attribution; you may not use it commercially or publish
modified/derivative versions. For other licensing, contact **hello@rundrill.com**.
