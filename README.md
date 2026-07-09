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

The two questions below matter most for this role. Ask these even if you skip others.

## Question A — Deployment depth + doing it the same way every time

- **What this checks (in plain words):** Can he take a messy, done-by-hand deployment and
  turn it into something clean that runs the same way every time? This is the actual day job —
  and it's the biggest gap in his resume, so dig in here.
- **Competency (library):** *Delivery Excellence / Senior Consultant* — produces high-quality
  work, spots and resolves risks, uses proper methods and tools.

- **Say this:** "Tell me about a time you had a setup that was done by hand — slow, messy, one
  step at a time — and you turned it into something clean that runs the same way every time.
  What was it? What security rules did you have to follow? And how did you make it easy to
  install, update, and keep track of?"
- **Follow-up (important):** "Do you write your setup as code — with tools like Terraform,
  Bicep, or Helm? How do you handle updates and keep an eye on things once it's live?"

- **Strong answer — he:**
  - names real tools (Terraform, Bicep, Helm, a CI/CD pipeline)
  - thinks about updates, rollback, and audit trails
  - does it the same way across many clients (repeatable, not one-off)
- **Weak sign — he:**
  - does deployments by hand
  - has no setup-as-code
  - can't explain how he watches it or undoes a bad change after go-live

## Question B — How he actually works with AI

- **What this checks (in plain words):** Does he really *work with* AI tools like Claude in his
  own day-to-day, or has he only *built products* that call an AI? And is he genuinely curious
  about it?
- **Competency (library):** *Knows the Business and the Industry / Consultant* — understands
  trends and learns leading practices.

- **Say this:** "Tell me about a recent time you used an AI assistant like Claude or Claude
  Code as a real part of getting engineering work done — not building a product feature, but in
  your own workflow. What were you trying to do, where did the tool break down or mislead you,
  and how did you handle that?"
- **Follow-up:** "Where do AI tools break, and how do you design around that?" / "What did you
  teach yourself recently, and what did you do with it?"

- **Strong answer — he:**
  - knows the difference between *building with* the AI and *working with* AI tools
  - is honest about where AI breaks (makes things up, forgets context, limited)
  - shows real, everyday curiosity about the field
- **Weak sign — he:**
  - only talks about AI as a product feature he built
  - treats AI as magic
  - can't name where it fails
