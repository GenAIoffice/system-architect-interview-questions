# System Architect — AI Engineering & Deployment: Interview Questions

Simple questions to read aloud. For each one: the question to ask, a follow-up, the good
answer you want to hear, and the weak answer to watch out for.

---

# Focus questions (ask these first)

These two matter most: deploying the same AI system into **different environments on a
customer's own cloud account**, repeatably, using setup-as-code (infrastructure-as-code).

## Question A — Deploying our app into a different customer's subscription (does he use IaC?)

**Ask this question:**
"Here's a real situation. We already have an application up and running in our own cloud
subscription. Now we want to deploy that same application into a **different customer's
subscription** — a separate cloud account that belongs to them. How would you do that? Would
you set it up by hand each time, or is there a better way?"

**Follow-up question:**
"Do you use infrastructure-as-code — tools like Terraform or Bicep — where the whole setup is
written as code? If yes, how would you take that same code and deploy it into a different
subscription for each new customer, just by changing a few settings? And how do you keep each
customer's environment separate from ours, and make sure they stay matched over time?"

**The good answer you want to hear:**
- He uses infrastructure-as-code (Terraform, Bicep) — the whole environment is written as code, not clicked by hand.
- He deploys the same code into a new customer's subscription by changing a few settings (subscription, names, region) — not rebuilding it.
- He keeps each customer's subscription fully separate — no shared data.
- He uses managed identities and a secrets vault instead of copying passwords or keys between subscriptions.
- He can repeat it quickly for the next customer, and has a way to keep environments matched (catch drift).

**The weak answer to watch out for:**
- He would set it up by hand, or copy things over manually, for each customer.
- He doesn't use infrastructure-as-code.
- He hardcodes names and settings, so each new customer needs a rewrite.
- He carries passwords or keys between subscriptions.
- No thought about keeping subscriptions separate, repeatable, or matched.

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
