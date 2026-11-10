# Delivery Methodology

How this course is taught — the pedagogy, the cadence options, and the facilitation stance. Read alongside `course-design.md` (the master design).

---

## 1. The pedagogy: problem-based learning (PBL)

Finance professionals learn by doing the work, not by watching slides about the work. Every module therefore opens with an **authentic problem** the participants recognise from their own desks — a blank budget template with a deadline, a messy ledger export before reconciliation, a possibly-unallowable cost. They then diagnose it, solve it with AI, *check the AI's work*, and present.

**No module is lecture-first.** Concepts (how a model hallucinates, what grounding is, what data classification means) are introduced only at the point they're needed to crack the problem in front of the group. This keeps every idea anchored to a use the participant already cares about.

### Why PBL specifically for AI + finance

1. **It forces verification.** When the goal is a *correct* deliverable, not "an AI output," learners naturally start checking the numbers — which is the single most important habit this course builds.
2. **It surfaces judgement.** Deciding *when not to use AI* only becomes real when you're holding an actual finance task with actual risk.
3. **It transfers.** Because problems mirror real work, participants can apply the same workflow to their own tasks the next day.

---

## 2. The session rhythm (every 2-hour block)

| Time | Phase | What happens | Facilitator role |
|---|---|---|---|
| 10 min | **Problem launch** | Present the scenario. No solution hints. | Set the stakes; resist explaining |
| 15 min | **Diagnose** | Groups define: what does a *good* answer need? What data? What could go wrong? | Circulate, ask probing questions |
| 55 min | **Work it** | Hands-on with AI, in pairs / small groups of 3–4 | Coach, don't rescue |
| 20 min | **Verify & critique** | Check the AI's numbers and claims against source | Make this non-negotiable |
| 20 min | **Share + reflect** | One group presents; debrief; each person logs one insight + one caution | Draw out the general lesson |

The **verify & critique** phase is the heart of the course. It is graded behaviour (see `assessment/rubric.md`), not an optional extra. If a cohort is running short on time, cut the *work* phase, never the *verify* phase.

---

## 3. Cadence options

The course is **20 contact hours**, deliverable three ways:

| Format | Structure | Best when |
|---|---|---|
| **Weekly (recommended)** | 10 sessions × 2 hrs over 10 weeks | PBL works best spaced — learners apply to real work between sessions |
| **Intensive** | 5 days × 4 hrs | Travel-in cohorts, residential workshops |
| **Hybrid** | 3 in-person days + 2 virtual follow-ups | Geographically split teams |

**Recommendation: the weekly/spaced version.** The biggest predictor of AI habits sticking is whether people use the tools on their *own* live tasks. Spacing forces that practice; an intensive risks a burst of enthusiasm that fades by the next reporting cycle.

If you must run intensively, pair each half-day with a **between-session micro-task** applied to the participant's real work, reviewed at the next block.

---

## 4. In-person vs virtual — what changes

Everything in this course works identically in both modes. The mechanics:

| Phase | In-person | Virtual |
|---|---|---|
| Diagnose | Flip chart / whiteboard per group | Shared doc or digital whiteboard, one per breakout |
| Work it | Groups at tables, laptops out | Breakout rooms of 3–4, screens shared within the room |
| Prompting demos | Facilitator screen on projector | Facilitator screen-share |
| Verify & critique | Groups swap and check each other's work | Swap docs across breakouts, or pair in main room |
| Share | Groups present at front | One group screen-shares to plenary |

**Virtual-specific tips:**
- Keep breakout groups to 3–4 so nobody disengages.
- Pre-load the synthetic datasets into a shared drive before the session.
- Build in a 5-minute buffer per transition — breakout logistics eat time.
- Record demos (not participant data) so learners can revisit prompting technique.

---

## 5. The facilitation stance

- **Coach, don't rescue.** When a group is stuck, ask "what does a correct answer need?" rather than giving the prompt.
- **Celebrate catching the AI.** When someone spots a hallucinated total or an invented regulation, make it the lesson of the session. The skill being built is scepticism, not fluency.
- **Model the red-lines.** Never bring real donor/salary/beneficiary data into the room. The course must practise what it teaches.
- **Localise live.** Especially in Module 5, swap in the cohort's actual donors and tax jurisdiction. Generic examples lose the experienced participants.
- **Mixed groups.** Blend senior finance staff with newer officers so they challenge each other's assumptions.

---

## 6. Materials checklist (per cohort)

- Synthetic datasets prepared and pressure-tested (see `facilitator-guide/synthetic-data/`)
- Deliberate "gotcha" failures seeded into demos (wrong total, invented rule, data-protection trap)
- Localised donor cost-principle excerpt + local tax provision for Module 5
- Access to at least one general-purpose AI assistant for every participant
- Printed or shared **Data Red-Line Card** (`resources/data-red-line-card.md`)
- Assessment rubric shared with participants up front (`assessment/rubric.md`)
