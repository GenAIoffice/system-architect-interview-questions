# System Architect — AI Engineering & Deployment: Interview Questions

Simple questions to read aloud. For each one: the question to ask, a follow-up, the good
answer you want to hear, and the weak answer to watch out for.

---

# Focus questions (ask these first)

These two matter most: deploying the same AI system into **different environments on a
customer's own cloud account**, repeatably, using setup-as-code (infrastructure-as-code).

## Question A — Deployment and doing it the same way every time

**Ask this question:**
"Tell me about a time you had a setup that was done by hand — slow and messy, one step at a
time. And you turned it into something that runs the same way every time, on its own. What was
it? What security rules did the client give you? And how did you set it up so it could be run
again somewhere new without doing it all over by hand?"

**Follow-up question:**
"Do you write your setup as code — with tools like Terraform, Bicep, or Helm? If a customer
wanted the same system inside their own cloud account, and in a few environments (like a test
one and a live one), how would you build it once and reuse it? And how do you make sure those
environments stay the same over time and don't drift apart?"

**The good answer you want to hear:**
- He writes the setup as code, so it builds the same way every time.
- He can reuse it for a new customer or a new environment by changing a few settings — not starting from scratch.
- He uses managed identities and a secrets vault — not shared passwords or keys copied around.
- He thinks about updates, undoing a change (rollback), and keeping a record (audit).
- He has a way to catch it when environments drift apart.

**The weak answer to watch out for:**
- He does deployments by hand.
- He doesn't write the setup as code.
- He would rebuild it from scratch for each customer or environment.
- He can't say how he watches it after go-live, or how he undoes a bad change.

## Question B — How he actually works with AI

**Ask this question:**
"Tell me about a recent time you used an AI tool like Claude or Claude Code as part of your own
work — not building an app feature, but to help you get engineering work done. What were you
trying to do? Where did the tool get something wrong or mislead you, and what did you do about it?"

**Follow-up question:**
"Where do AI tools usually break or fall short, and how do you work around that? And what's
something you taught yourself recently, and what did you do with it?"

**The good answer you want to hear:**
- He really uses AI tools in his day-to-day work, not as a gimmick.
- He knows the difference between building an app that calls an AI and actually working with AI tools.
- He's honest about where AI fails (makes things up, forgets context, has limits).
- He's genuinely curious and keeps learning.

**The weak answer to watch out for:**
- He only talks about AI as a feature he built into a product.
- He treats AI as magic that never gets things wrong.
- He can't say where it fails.

---

# Other questions (ask if there's time)

## Question C — Solving problems with no map

**Ask this question:**
"Tell me about a time you had to build or set something up where there was no guide, no example
to copy, and no clear right answer. What was the hard part? How did you break it down, what did
you try first, what went wrong, and how did you finally land on something that worked?"

- **Good answer:** breaks a big unknown into pieces, tries a small version, learns from what breaks, lands on something solid.
- **Weak answer:** only smooth stories; waited for someone else to tell him how.

## Question D — Making his work usable by other people

**Ask this question:**
"A lot of your work has been solo. Tell me about a time you wrote a guide, a runbook, or a
handoff so other people could run something you built without you. How did you know it actually
worked for them? And tell me about a time you pushed back on a design decision — even one of
your own."

- **Good answer:** other people really could run his work; he documents on purpose; he disagrees with good reasons and no ego.
- **Weak answer:** "it's all in my head"; docs are an afterthought; he gets defensive.

---

*SHARE format reminder — probe for: Situation, Hindrance, Action, Result, Evaluation.*
