# Startup product engineering interview track

Goal: independently take an ambiguous customer problem through scoping, implementation, launch, and measurement, and explain the reasoning in an interview.

Learner context: React basics, rusty after three years of AI-assisted coding. Available time: up to two hours daily. Goal: interview as soon as practical. Target companies and role level are still unknown.

Recommended stack: TypeScript, React, Next.js, and PostgreSQL. Keep JavaScript, HTTP, SQL, and browser fundamentals explicit. This builds on existing knowledge; it is not a claim that all startups use this stack. A current AthenaHQ product-engineer listing includes React, Next.js, and TypeScript: https://www.ycombinator.com/companies/athenahq/jobs/EAoJcox-product-engineer

## Two-hour daily loop

- 15 minutes: retrieve yesterday’s concepts and explain a short code snippet without AI.
- 25 minutes: one adaptive LearnHarness lesson on a demonstrated gap.
- 60 minutes: implement or debug one small feature. Attempt it independently first; use AI for targeted hints and review after recording the attempt.
- 20 minutes: test edge cases, explain tradeoffs aloud, and record evidence and next steps.

## Initial 14-day sprint (28-hour ceiling)

Days 1–3: JavaScript/TypeScript and React state, forms, effects, async behavior, and error handling. Build a local feedback list and explain each part.

Days 4–6: HTTP, Next.js request handling, PostgreSQL schema/queries, validation, and one persisted vertical slice.

Day 7: timed feature exercise and review; revise the next week based on observed gaps.

Days 8–10: ownership checks, retries/duplicate writes, debugging, risk-focused tests, and useful product metrics.

Days 11–12: a small ambiguous product task and practical system-design rehearsal; practice core arrays/maps/complexity in the coding block.

Days 13–14: mock feature/debugging interview, a project walkthrough, and an evidence-based decision about interview readiness.

This is a diagnostic sprint, not a promise of readiness in two weeks. Begin identifying roles immediately and tailor preparation to actual interview formats. Prioritize a narrow working feature over capstone breadth.

## Learning sequence

1. Baseline: scope a customer request, explain a browser-to-database request, and diagnose a duplicate-write incident. Use the reasoning to choose the first lesson.
2. Product judgment: user and pain point, success metric, smallest useful release, explicit exclusions, and ways to validate assumptions.
3. Vertical delivery: accessible UI states, API contracts, data modeling, validation, authentication versus authorization, and meaningful tests.
4. Reliability: retries, idempotency, race conditions, migrations, logs, failure diagnosis, and safe rollout/rollback.
5. Product iteration: instrumentation, activation and retention, qualitative feedback, experiments, and prioritization under limited time.
6. Interview rehearsal: timed feature work, debugging, pragmatic system design, and project/ownership stories. Include coding fundamentals according to target interview formats.

Progress by demonstrated reasoning and implementation, not lesson completion. After a topic, solve a different scenario without hints; return to it in a later session. Track observations in a separate practice log; the knowledge graph records concepts and reasoning, not mastery.

## Suggested capstone

Build a small customer-feedback triage tool: submit feedback, tag it, assign an owner, and change status. Start with one end-to-end flow. Later introduce duplicate submissions, cross-workspace access, concurrent updates, and a rollout incident. Use TypeScript, React, Next.js, and PostgreSQL, adapting the scope after calibration.

Deliverables: a one-page scope, working vertical slice, a few risk-focused tests, a short launch/measurement plan, and a five-minute tradeoff explanation.

## First LearnHarness teaching-session prompt

I want to learn product engineering for startup interviews. My background is React basics, rusty after three years of AI-assisted coding. I have up to two hours daily and want to interview as soon as practical. Use TypeScript, React, Next.js, and PostgreSQL as the proposed stack. Ask only for missing target-role context before probing. Then probe my reasoning one question at a time, starting with the scenario below. Do not infer competence from confidence or supply the solution before I attempt it. Build a dependency plan from observed gaps. Teach one idea at a time, ask me to predict behavior, and use a fresh scenario to check transfer. Include product judgment, implementation, debugging, reliability, and communication. Distinguish simplifications from production requirements. Do not claim knowledge-graph membership proves mastery.

Scenario: A B2B startup's customers lose feature requests in Slack. A founder asks for a feedback dashboard by Friday. What would you clarify first, what would you ship, what would you leave out, and how would you know it helped?

## Follow-up practice-session prompt

Give me one unfamiliar startup product-engineering problem at a time using concepts from my completed teaching sessions. Mix scoping, coding, debugging, design, and communication without naming the concept being tested. Have me state assumptions and reason aloud. Withhold the solution until I submit an attempt or request it. Then give specific feedback on correctness, user value, simplicity, failure handling, verification, and explanation. Label hints and distinguish independent performance from assisted performance. Adapt the next problem to the evidence.

## Running the app

The fork is [anikam13/learnharness](https://github.com/anikam13/learnharness). Run the commands below from its local checkout.

Run `npm ci`, then `npm run dev` from the checkout. Open http://localhost:3000. Configure a provider connection and model slots in the app; credentials must be supplied by you through its settings. Start a teaching session with the prompt above. Use practice after there is actual material to practice.
