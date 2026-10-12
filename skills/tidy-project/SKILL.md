---
name: pm-skills:tidy-project
description: Review and improve an existing project, or work through a team's projects one at a time, until scope, ownership, success measures, timing, and updates are clear. Use with Linear, another connected project management tool, or pasted project details.
---

# Purpose

Guide a PM from an incomplete project to one that is clear, current, and ready to coordinate around. Identify substantive gaps, help resolve them, and update the project when authorized.

# When to use

- Cleaning up a project before planning or a roadmap review
- Working through a team's projects one at a time
- Refreshing stale scope, ownership, dates, milestones, or progress updates

# Inputs

- A project link, a team or portfolio link, or pasted project details
- Optional team conventions, readiness criteria, project stage, or review scope
- Optional supporting evidence, such as project documents or recent updates
- Local context from `~/.config/pm-skills/config.yml` or `~/.pm-skills/config.yml` when available

# Instructions

## Find the project and establish scope

- Use local context only for defaults like team, role, product area, and timezone. Do not treat it as project evidence.
- A supplied link or named tool determines which connection to use. Otherwise check whether Linear is connected. If it is unavailable, ask which project management tool or MCP to use, or accept pasted details. Do not require Linear or install a connection automatically.
- Check the available tool's actual read and write capabilities. If it cannot access the requested project, explain the limitation and ask for access or pasted details. If it can read but cannot write, continue the review and provide ready-to-paste edits.
- For a team or portfolio, list projects within the requested scope, following pagination when available. State any incomplete coverage. Keep a compact queue of projects reviewed, current, remaining, or skipped, and work through one at a time. Honor the user's order; otherwise start with an active project with obvious gaps.
- Read the selected project's fields, description, linked scope documents, and recent updates as needed. Keep evidence gathering scoped to that project; do not search every connected source by default.
- If given an issue link, explain the project focus and offer to review its parent project or adapt the checks to the issue. Do not silently expand an issue request into a team-wide review.
- Adapt the checks to project stage and explicit team conventions. Discovery and internal projects are not universally excluded. Treat campaign-specific exclusions, labels, or deadlines as applicable only when the user adopts those rules.

## Assess readiness

Use the following defaults, adjusted to the agreed scope. Assess the usefulness and consistency of the information, not merely whether fields are populated.

| Check | What good looks like |
|---|---|
| Owner and team | One accountable owner, plus the participating team and relevant contributors. Use a team lead default only when the team's convention supports it. |
| Classification | The relevant mission, strategic connection, or project type where useful. Organization-specific labels such as Mission, Big Bet, or Internal are conventions, not universal requirements. |
| Scope | A concise, roughly one-page explanation of the problem, affected users, intended solution, and boundaries. Preserve useful detail in linked documents. |
| Success | Meaningful success measures with known baselines and agreed targets, including how and when they will be assessed. For discovery, agree on the learning or decision needed rather than inventing a launch outcome. |
| Timing | A credible start and target date or period. Preserve month or quarter precision when that is all the evidence supports; distinguish an estimate from a commitment and avoid placeholder dates. |
| Milestones | Useful outcomes, dependency deadlines, or rollout checkpoints. Optional by default, recommended for work longer than four weeks or with complex dependencies. |
| Progress update | A current account of progress, next steps, and material risks or blockers. Use the team's cadence, defaulting to weekly for active projects. A kickoff update can establish the starting point for new work. |

- Map information to the tool's native fields where possible, or to its project description or an appropriate project document. For a Basecamp-style workspace without equivalent labels or metric fields, a short project brief can hold the same information. Verify available capabilities rather than assuming a particular tool supports them.
- Separate `Met`, `Gap`, `Not verified`, and `Not applicable`. Give a brief reason for inapplicable checks. Unsupported fields do not make the underlying information inapplicable; find a suitable home when it matters.
- Distinguish required gaps from optional recommendations. Recommended milestones do not block readiness unless the user or team makes them a requirement.
- Missing baselines, targets, dates, or evidence remain visible gaps until resolved or explicitly made inapplicable for a sound reason. A plan to obtain missing information is useful progress, but does not establish that information.
- For dormant or finished projects, establish whether the lifecycle status is accurate before polishing delivery details. Propose an appropriate status change when supported by evidence; do not close, pause, or cancel projects merely to improve readiness counts.

## Help resolve the gaps

- This skill is conversational. Present a short assessment and the most useful next step, then ask one or two focused questions at a time. Use information already gathered; do not repeat a full interview or force every project through every supporting skill.
- Address foundational gaps before cosmetic edits: clarify the problem and scope before deriving measures or dates. Resolve small gaps directly.
- When a gap needs more work, explain the benefit of a relevant supporting skill and offer to use it. Carry the current project context and evidence into the exercise, then return to this review with the result.

| Gap | Supporting skill | Intended contribution |
|---|---|---|
| Unclear problem, users, or impact | `pm-skills:frame-problem` | Establish the problem and evidence before shaping a solution. |
| Vague solution, scope, or success direction | `pm-skills:shape-product-pitch` | Develop a bounded proposal and useful success signals. |
| Missing baseline, target, or measurement approach | `pm-skills:measure-impact` | Define a credible way to assess the intended outcome. |
| Weak dates, sequencing, or milestones | `pm-skills:estimate-timeline` | Work through dependencies, rollout, and scope tradeoffs. |
| Missing or stale project update | `pm-skills:team-status` | Draft an update restricted to this project's progress, risks, and next steps. |
| A requested update on personal contributions | `pm-skills:my-status` | Clarify the individual's progress, next steps, and asks. |

- Read a supporting skill when using it, through the installed skill or its sibling `../<skill-name>/SKILL.md` in this repo, and preserve the selected project and tool scope. Its preferred source or output conventions must not expand the review. For example, do not search unrelated team work for a project update or require an MMDD shorthand to pass readiness.
- Supporting skills are optional. If unavailable, continue with focused questions and draft the relevant project content without claiming that the skill ran.
- If the user asks to fast-track, use available evidence and ask only for material missing inputs. Keep unresolved items explicit.
- Never invent owners, stakeholder agreement, progress, metrics, dates, or evidence. Label proposed choices as proposals until confirmed. Do not rewrite sound existing content just to match a template.

## Apply changes and verify

- Review or draft requests do not authorize external edits. Prepare concrete field changes and text before asking for any needed authorization. Honor explicit instructions to update the project and authorization already given; do not repeatedly ask for the same permission.
- Use an existing appropriate destination for scope and progress content. Identify the destination before creating a new document or publishing an update. Project cleanup does not authorize messages to unrelated channels or people.
- Before writing, check that the relevant project content has not changed since the review and reconcile any newer information. Preserve unrelated fields and useful existing text.
- Make only the authorized changes. Read them back and rerun the affected readiness checks. If a write fails or its outcome is uncertain, inspect the current state before retrying; avoid duplicate updates or documents.
- Distinguish changes applied, drafts prepared, and changes that failed or could not be verified. If all applicable checks are satisfied only in prepared edits, report `Ready in draft`. Report `Ready — verified in project` only after the tool confirms the required information is present. Otherwise report `Needs input` or `Verification needed` and name the remaining gaps.
- After finishing a project, update the queue and offer to continue to the next one. If the user already asked to work through the whole queue, continue within that scope, pausing only for needed input or authorization.
- Run upkeep when invoked. Do not create recurring monitoring or automations unless requested.

## Present the result

- Use `examples/output.md` as the canonical review shape. Keep the title unnumbered, followed immediately by a concrete `**tl;dr:** ...` stating readiness and the main remaining gap or completed improvement.
- Follow with sequential numbered sections: `Readiness`, `Changes`, and `Next Step`. Use a compact readiness table with `Check`, `Status`, and `Evidence or gap`. Group related checks when their status is the same and the meaning remains clear.
- In `Changes`, distinguish proposed edits from applied and verified edits. Show exact replacement text or field values when preparing changes for review or manual use. Do not duplicate lengthy existing content.
- In `Next Step`, give the focused question, useful skill suggestion, or next project. For a queue, include brief progress and make skipped projects distinguishable from completed ones.
- Use short paragraphs for coherent points and numbered lists for distinct items. If any item in a numbered list has multiple sentences, bold the first sentence of every item in that list; otherwise leave the list unbolded. Do not use bold labels as substitute section headings.
- Link projects and supporting evidence when URLs are available. Keep the review concise, usually under 400 words excluding replacement content. Do not claim readiness merely because edits were attempted.

# Output

A concise project readiness review, concrete improvements or applied changes, and a guided next step toward resolving the remaining gaps. For a team or portfolio, preserve a visible queue and complete the review one project at a time.
