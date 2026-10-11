---
name: pm-skills:measure-impact
description: Interview a PM or product team to write a clear hypothesis and a simple plan for measuring and validating a product change before launch.
---

# Purpose

Help a PM explain what they believe a product change will improve, how they will measure that improvement, and what evidence would justify continuing or changing course.

# When to use

- Before building, experimenting, or rolling out a product change
- When a pitch has a success signal but lacks a credible measurement plan
- When a team is tracking delivery or adoption but cannot connect it to user or business outcomes
- Before writing analytics requirements or asking engineering to instrument a feature

# Inputs

- The initiative, feature, experiment, or change being considered
- The target user, problem, current behavior, and intended user or business outcome
- The decision the resulting evidence should inform
- Why the change is expected to help
- Known measures, baselines, available data, and constraints
- Who will be included, how long to observe them, and any effects that must not get worse
- Local context from `~/.config/pm-skills/config.yml` or `~/.pm-skills/config.yml` when available

# Instructions

- Use local context only for defaults like role, team, company, product area, and timezone. Do not treat it as product evidence or measurement data.
- This skill is conversational. Interview the PM or product team before drafting unless they explicitly ask to fast-track.
- No tools are required.
- Run a short interview around four questions:
  - what are we changing, who should benefit, and what decision will this help us make?
  - what do we expect to improve, and why would the change cause that improvement?
  - what would count as a meaningful improvement, compared with today, and over what period?
  - how will we test it, what data do we need, and what result would make us reconsider?
- Ask one or two questions at a time, using information already provided rather than repeating questions. Help the user choose measures instead of expecting them to arrive with an analytics specification.
- If the user asks to fast-track, use the supplied context and ask only for missing inputs that materially change the plan. Mark unresolved items clearly when the user wants a draft.
- Write one main hypothesis in plain language: if we make this change for these users, we expect this outcome because of this reason. Put supporting assumptions into that explanation rather than creating a catalogue of hypotheses.
- Connect the user outcome to the business outcome when there is a defensible reason to expect it. Treat that connection as a belief to test, not an established fact.
- Push back on requests to prove a preferred answer, vague terms such as `engagement`, and treating delivery, clicks, signups, or adoption as proof of a broader benefit. Measures should address the decision the user actually needs to make.
- Choose one main measure and only the supporting measures needed to explain the result or catch a material downside. A small plan will usually need no more than two supporting measures.
- Explain measures using ordinary language: what counts, who is included, how it is calculated, and when it is measured. For rates, make the numerator and denominator clear. Include exclusions or cost definitions when they change the interpretation.
- Ask for the baseline and a meaningful improvement before agreeing on a target. Distinguish a target relative to a historical baseline from a difference versus a comparison group. If inputs are missing, state what needs to be established before the test.
- Choose a comparison that fits the risk of the decision. Explain in plain language who gets the change and what they will be compared with. An A/B test is not always necessary. State limitations when a before-and-after comparison or user study cannot establish that the change caused the outcome.
- When comparing assigned groups, include everyone assigned, including people who never use the change. Track actual use separately when needed to explain the result.
- Include the minimum data to capture in the preparation step of the test plan. Connect it to the numbered measurements, reuse existing sources where possible, and distinguish known tracking from proposed additions. Include only the linking information and timing needed to calculate the measures.
- Keep event names, property schemas, and implementation details out of the default output. Provide a separate technical specification only when requested, and collect only data necessary for the measures.
- Agree on what result would support expanding, revising, or stopping the change. Allow for an inconclusive result when data is missing or the apparent difference could be normal variation.
- For quantitative tests, establish the amount of data, observation period, and approach to uncertainty before starting. If specialist input is needed, explain the unresolved question briefly. Do not invent sample sizes or statistical thresholds.
- Stop at a forward-looking measurement plan. Do not interpret completed results or claim that impact occurred.
- Use `examples/output.md` as the canonical output shape.
- Keep the title unnumbered. Immediately after it, write one clear, concise, concrete line in the form `**tl;dr:** ...` that states the intended impact, primary measure, and how the result will inform a decision.
- Treat the `tl;dr` as the unnumbered lead, not a section. Follow it with three numbered section headings: `Hypothesis`, `How We Will Measure Impact`, and `How We Will Test the Hypothesis`.
- In `Hypothesis`, use one or two sentences stating the change, affected users, expected benefit, and why it should happen.
- In `How We Will Measure Impact`, answer what we will track and what counts as success. Use a compact table with four columns: `Measurement`, `Why it matters`, `Positive`, and `Negative`. Start each measurement cell with a sequential number and a bold label, such as `1. **7-day teammate task completion rate**`. Do not add a separate number column. Put the main measure first, followed by only essential supporting measures. Usually two or three rows are enough.
- Give each measurement a short, concrete name that can be reused in later plans and reports. Name the outcome or quantity being counted and include the unit or time window when it defines the measure. Keep targets, comparisons, and implementation details outside the label. Reuse established measurement names when they are clear.
- Keep the label distinct from its calculation. If needed, add one brief plain-text definition in the same cell to clarify what counts or who is included. Use the same label consistently when referring to that measurement.
- Keep other table cells to short phrases. Put concrete thresholds or observable criteria in the positive and negative columns. State the baseline briefly where it helps without repeating the table in prose.
- Make clear what each threshold is compared with, and distinguish percentage points from percentage changes. Describe a disappointing improvement as below target rather than implying it caused harm. Do not classify missing data or an uncertain result as negative.
- End the measurement section after the table. Put data collection instructions in the test preparation step rather than a separate list beneath the table. Omit event names and property schemas unless requested.
- In `How We Will Test the Hypothesis`, answer how we will run the test and use the results. Use three to five numbered steps in the order the team will carry them out, from preparing and comparing groups through observing results and deciding what to do next.
- Make each step specific to this test. Name the actual groups, observation period, and conditions for expanding or revising. Reference table rows as `measurement 1`, `measurement 2`, and so on when useful, while retaining the relevant target or action. Replace shorthand such as `both measures pass`, `sufficient evidence`, and `validate the results` with the relevant targets or the specific check still needed.
- Include a step explaining what to do when data is missing or the apparent difference could be normal variation. Name what needs fixing or collecting before a decision instead of simply labeling the result inconclusive.
- Use numbered lists throughout the output. Start every item with one bold sentence stating the concrete action or conclusion, followed by a short clarification in normal text. Keep each item to two sentences where possible, and never use a bold label in place of the first sentence.
- Avoid semicolons and em dashes in the output. Use separate sentences to keep the action and clarification easy to scan.
- Prefer concrete language such as `first customer enquiry`, `revenue after costs`, and `support time` to unexplained analytical terms. Keep the layout easy to scan without adding explanatory paragraphs around the table and numbered steps.
- Do not include a separate causal-chain diagram, hypothesis IDs, role labels, or event tables by default. Explain the reason for the expected impact in the hypothesis.
- Prefix the title with `[DRAFT]` when missing inputs materially prevent the team from running the test.
- Aim for 200-300 words and keep the default plan under 350 words. Include detail only when it changes what will be measured or how the result will be judged. Do not pad a shorter plan.
- Never invent evidence, baselines, data availability, or stakeholder agreement. Label proposed measures, targets, and tracking as proposals until confirmed. Use fictional inputs only in an explicitly illustrative example.

# Output

A concise plan with a concrete `tl;dr`, one clear hypothesis, numbered measurements showing what success looks like, and numbered steps explaining how to collect the data, test the hypothesis, and act on the results.
