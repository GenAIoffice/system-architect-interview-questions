# System Architect — AI Engineering & Deployment: Interview Questions

Plain-English questions to read aloud. Under each: what a strong answer sounds like, and
weak signs to watch for.

---

## Q1 — How he works with AI (opener)

**Say this:** "Tell me about something technical you taught yourself recently. What made you
want to learn it, and what did you do with it? And do you use AI tools like Claude or Claude
Code in your day-to-day work? Walk me through a time it helped — and a time it got something
wrong and you had to catch it."

- **Strong answer:** real curiosity; uses AI tools as part of how he works; honest about where they fail.
- **Weak sign:** only talks about AI as a product feature he built; acts like it never gets things wrong.

---

## Q2 — Solving problems with no map

**Say this:** "Tell me about a time you had to build or set something up where there was no
guide, no example to copy, and no clear right answer. What was the hard part? How did you
break it down, what did you try first, what went wrong, and how did you finally land on
something that worked?"

- **Strong answer:** breaks a big unknown into pieces, tries a small version, learns from what breaks, converges on something solid.
- **Weak sign:** only smooth stories; waited for someone else to tell him how.

---

## Q3 — Turning a messy deployment into a clean, repeatable one

**Say this:** "Tell me about a time you had a setup that was done by hand — slow, messy, one
step at a time — and you turned it into something clean that runs the same way every time.
What was it? What security rules did you have to follow? And how did you make it easy to
install, update, and keep track of?"

**Follow-up:** "Do you write your setup as code — with tools like Terraform, Bicep, or Helm?
Once it's live, how do you watch it, and how do you undo a change if something breaks?"

- **Strong answer:** names real tools; thinks about updates, rollback, audit trails, doing it the same way across many clients.
- **Weak sign (gap in his resume — listen closely):** deployments all manual; no setup-as-code; can't explain how he monitors after go-live.

---

## Q4 — Making his work usable by other people

**Say this:** "A lot of your work has been solo. Tell me about a time you wrote a guide, a
runbook, or a handoff so that other people could run something you built without you. How did
you know it actually worked for them? And tell me about a time you pushed back on a design
decision — even one of your own."

- **Strong answer:** other people really could run his work; documents on purpose; disagrees with good reasons and no ego.
- **Weak sign:** "it's all in my head"; docs are an afterthought; gets defensive.

---

## Q5 — The deployment scenario (real job, product never mentioned)

**Say this:** "Here's a situation. You have an AI app that already works well in one cloud
account. Now a client in a regulated industry — say a bank — wants the same app running inside
their own private cloud account. Their rules: their own security, their own logins, no shared
passwords or keys, and every action has to be recorded for audit. And you want to set it up so
the **next** client after them is quick — not a fresh start each time. How would you do it?
Where would you start, and what would you be most careful about?"

**Follow-up:** "How would you make sure the new setup matches the first one exactly — and
stays matched over time, with nothing quietly drifting apart?"

- **Strong answer:** writes everything **as code** (built from a template, not by hand); uses
  **managed identities + a secrets vault** instead of shared keys; keeps each client **fully
  isolated**; turns on **audit logging** from day one; packages it so the next client is just
  "run the template again" with a few settings changed; stops drift with **same code for every
  environment + automated checks** that compare live setup to the code.
- **Weak sign:** copies things over by hand; carries passwords/keys between environments;
  treats each client as a one-off; no audit trail; no drift checking.

---

*SHARE format reminder — probe for: Situation, Hindrance, Action, Result, Evaluation.*

---
---

# Focus questions (A & B)

These two matter most for this role — deploying the same AI system into **different
environments on a customer's own cloud subscription**, repeatably, using infrastructure-as-code.
Ask these even if you skip others.

## Question A — Deployment / operations depth + repeatability (directly tests the IaC / platform gap)

**Competency (library):** *Delivery Excellence / Senior Consultant* — "high quality work
product... identifies and resolves risks... uses approved methodologies and tools."

**Ask:** "Tell me about a manual or bespoke deployment you turned into a repeatable, defensible
process. What was the environment, what constraints did the client/security team impose, and
how did you make it install, configure, upgrade, observe, and audit reliably across
environments — including standing the same system up inside a customer's own cloud subscription?"

**Probe (crucial):** "How do you use infrastructure-as-code — Terraform, Bicep, Helm — to stand
up the same system across different environments (dev / test / prod) and across different
customer subscriptions? How do you keep those environments matched, handle upgrade paths, and
cover observability and incident tooling?"

**Meets:** names concrete IaC / release / observability tooling; parameterizes per environment
and per customer subscription; thinks about upgrades, rollback, audit trails, and
*repeatability across environments and clients*.

**Does not meet:** deployments are ad-hoc/manual; no IaC; rebuilds per environment instead of
parameterizing; can't describe observability, drift control, or upgrade strategy.

## Question B — AI fluency & how he actually works with AI tools

**Competency (library):** *Knows the Business and the Industry / Consultant* — "understand...
interpret sector trends, and learn leading practices."

**Ask:** "Tell me about a recent time you used an AI assistant like Claude or Claude Code as a
real part of getting engineering work done — not building a product feature, but in your own
workflow. Walk me through the situation, what you were trying to do, where the tool broke down
or misled you, and how you handled that."

**Probe:** "Where do LLMs break, and how do you design around that?" / "What did you teach
yourself recently and what did you do with it?" (his application note)

**Meets:** distinguishes building with the API from working with agentic tools; concrete
workflow; honest about failure modes (hallucination, context limits); genuine curiosity.

**Does not meet:** only talks about the API as a product ingredient; treats AI as magic; can't
name where it fails.
