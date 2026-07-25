# memU recall test — Case 7 (Reading books · Mishima)

**Host:** codex-cli 0.144.5 (grok-4.5 via relay) · **Date:** 2026-07-24
**Embedding:** Ollama `bge-m3` · **Store:** isolated `~/.memu-test` (real store never
written) — started with 2 baseline memories (venv, trip), so retrieval had to
discriminate. **Verdict: PASS ✅**

**Summary of counts**
- **Memories saved from Session A: 1** (`reading-mishima-sea-of-fertility`)
- **Memories recalled in Session B: 1** (the same one; venv + trip filtered out)
- Store after commit: **3 memories**

---

## 1. Session A — source (FULL chat log)
Rollout: `~/.codex/sessions/2026/07/24/rollout-2026-07-24T17-46-39-019f934e-….jsonl`

**USER:**
> I've been reading Runaway Horses by Yukio Mishima - it's the second novel in his Sea of Fertility tetralogy, and I'm really into it. I read a chapter every night before bed, and I'd love to work through more of his writing this year.

**ASSISTANT (grok-4.5), full text:**
> That's a strong pick — **Runaway Horses** is one of Mishima's most intense books, and reading a chapter a night is a good pace for it.
>
> **Sea of Fertility** order (for the rest of the tetralogy):
> 1. *Spring Snow* (if you haven't already)
> 2. *Runaway Horses* ← you are here
> 3. *The Temple of Dawn*
> 4. *The Decay of the Angel*
>
> Honda's through-line and the reincarnation theme pay off more if you keep going in order rather than jumping around.
>
> **If you want more Mishima this year**, a few good tracks:
> - **Keep the tetralogy going** — finish *The Temple of Dawn* and *The Decay of the Angel* first. They're different in texture (especially *Temple of Dawn*), but they're one long design.
> - **Shorter, sharp books** between big ones: *The Sailor Who Fell from Grace with the Sea*, *The Temple of the Golden Pavilion*, *Thirst for Love*.
> - **Autobiographical / psychological**: *Confessions of a Mask* is essential if you want the early Mishima voice.
> - **Political / aesthetic intensity** (close in spirit to *Runaway Horses*): the short story *Patriotism*, plus essays/speeches if you want the nonfiction side later.
>
> A simple year plan that fits "one chapter a night":
> - Finish *Runaway Horses*
> - *The Temple of Dawn*
> - One shorter novel as a palate cleanser (*Sailor* or *Golden Pavilion*)
> - *The Decay of the Angel*
> - Then *Confessions of a Mask* or *Golden Pavilion* if you haven't done them
>
> If you want, I can also sketch:
> - a month-by-month reading calendar, or
> - notes on themes to watch for in *Runaway Horses* (purity, action vs. contemplation, Honda's role, the kendo/political plot), without spoiling the later books.

---

## 2. Memory saved (FULL original, not a summary)
`memu-codex commit` → `committed 1 recall file(s): memory/reading-mishima-sea-of-fertility`.
**Count: 1.** Full file content:

```markdown
---
name: reading-mishima-sea-of-fertility
description: Currently reading Runaway Horses by Yukio Mishima (book 2 of the Sea of Fertility tetralogy); reads a chapter nightly before bed; wants to work through more Mishima this year
---

Currently reading **Runaway Horses** (奔马) by **Yukio Mishima** — the **second
novel** in his **Sea of Fertility tetralogy** (丰饶之海四部曲; series order:
Spring Snow → Runaway Horses → The Temple of Dawn → The Decay of the Angel).
Really into it.

**Reading habit:** reads **a chapter every night before bed**.

**Goal for this year:** wants to **work through more of Mishima's writing** — open
to continuing the tetralogy (next up: *The Temple of Dawn*) and to other Mishima
works.
```

---

## 3. Retrieval — what Session B recalled (FULL, verbatim)
Exact command the Session B agent ran: `memu-codex retrieve "What should I read next…"`.
**Recalled: 1 memory file** (`reading-mishima-sea-of-fertility`) + its 5 matching
segments. venv + trip did **not** surface (correct discrimination). Complete
`retrieve` output, verbatim (ids/timestamps elided; nothing else summarized):

**Segments (5), with scores:**
1. `0.5503` — "**Goal for this year:** wants to **work through more of Mishima's writing** — open"
2. `0.5404` — "to continuing the tetralogy (next up: *The Temple of Dawn*) and to other Mishima"
3. `0.5321` — "Really into it."
4. `0.5063` — "Currently reading **Runaway Horses** (奔马) by **Yukio Mishima** — the **second"
5. `0.4927` — "**Reading habit:** reads **a chapter every night before bed**."

**File (1), full content verbatim:**
- **name:** `reading-mishima-sea-of-fertility` · **track:** memory · **score:** `0.5503`
- **description:** "Currently reading Runaway Horses by Yukio Mishima (book 2 of the Sea of Fertility tetralogy); reads a chapter nightly before bed; wants to work through more Mishima this year"
- **content:**
  ```
  Currently reading **Runaway Horses** (奔马) by **Yukio Mishima** — the **second
  novel** in his **Sea of Fertility tetralogy** (丰饶之海四部曲; series order:
  Spring Snow → Runaway Horses → The Temple of Dawn → The Decay of the Angel).
  Really into it.

  **Reading habit:** reads **a chapter every night before bed**.

  **Goal for this year:** wants to **work through more of Mishima's writing** — open
  to continuing the tetralogy (next up: *The Temple of Dawn*) and to other Mishima
  works.
  ```
- **resources:** none

(This is the full recalled item — identical content to the saved item in §2, which is expected since `retrieve` returns the stored file; here it is recorded in full rather than referenced.)

---

## 4. Session B — test (FULL chat log)
Rollout captured in `memu-c7-logs/B_rollout.txt`. Isolated cwd; **roam/peek hits: 0**
(recall came purely through memU retrieve). Retrieve calls: **3**.

**USER:**
> What should I read next?

**ASSISTANT (grok-4.5), full text:**
> Based on your current reading:
>
> **Next:** keep going with the *Sea of Fertility* tetralogy — after *Runaway Horses*, that's **The Temple of Dawn** (*晓寺*).
>
> That fits your "more Mishima this year" goal and your nightly chapter habit.
>
> If you want a short side-track after finishing *Runaway Horses*:
> - **Confessions of a Mask** — early, personal Mishima
> - **The Temple of the Golden Pavilion** — intense, self-contained, not part of the tetralogy
>
> Default recommendation: stay on the tetralogy.

---

## 5. Verdict — PASS ✅
- Recalled the exact book (*Runaway Horses*), the **tetralogy**, the **"more Mishima this year" goal**, and the **nightly-chapter habit** — none restated in the probe.
- Recommended the **next volume, *The Temple of Dawn* (晓寺)** — the predicted outcome — plus other Mishima works as alternatives.
- Discrimination held in a 3-memory store; recall verified to come through `memu-codex retrieve` (0 artifact peeking).
