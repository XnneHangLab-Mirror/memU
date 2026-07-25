# memU recall test — extended scenes

Extends the originals (Case 4 recurring-bug, Case 5 travel, Case 6 writing-style),
same shape: **Session A** plants a fact, a fresh **Session B** probes it. Each case
states what should be **remembered** and **recalled**, then the exact lines the user
says.

---

## Case 7 — Reading books
* **Remember:** reading *Runaway Horses* (奔马) by Yukio Mishima (三岛由纪夫) — book 2 of the *Sea of Fertility* tetralogy (丰饶之海四部曲); loves his writing; reads a chapter nightly before bed; wants to work through more of his writing this year.
* **Recall:** recommend a fitting next read — the next book in the tetralogy (*The Temple of Dawn* / 晓寺) or another Mishima work.

Session A (source)
* Opening: "I've been reading Runaway Horses by Yukio Mishima — it's the second novel in his Sea of Fertility tetralogy, and I'm really into it. I read a chapter every night before bed, and I'd love to work through more of his writing this year."

Session B (test)
* Opening: "What should I read next?"
* PASS: reflects Mishima / the Sea of Fertility tetralogy (suggests *The Temple of Dawn* or another Mishima work), not a generic list.

## Case 7.5 — Reading books (mid-book, character-level, spoiler check)
* **Remember:** partway through *Runaway Horses*; taken with the character **Isao Iinuma (饭沼勋)**, the intense young idealist, at the point where he's gathering his followers.
* **Recall:** recall the character Isao and encourage reading on — WITHOUT spoiling his fate (the key observation: does the agent 剧透 / spoil?).

Session A (source)
* Opening: "I'm about a third into Runaway Horses and I'm really taken with Isao — this intense young idealist. Right now he's just started gathering his group of followers."

Session B (test)
* Opening: "I'm so invested in Isao now — should I keep going, and where's his story headed?"
* PASS: recalls Isao + encourages continuing; does NOT spoil his fate. (Observe whether it drops a spoiler.)

---

## Case 8 — Playing games (two remember points)
* **Remember 1 — playstyle / setup:** plays *The Elder Scrolls V: Skyrim* on PC, heavily modded; runs a **stealth-archer Khajiit** build (sneak, archery, light armour).
* **Remember 2 — progress / blocker:** partway through the **Dragonborn DLC**, hard **stuck on Miraak**; only gets to play on **weekends**.
* **Recall:** identify the boss (Miraak, in Skyrim) **and** tailor the advice to the stealth-archer build.

Session A (source)
* Opening: "I've been playing Skyrim on PC — heavily modded — and I run a stealth-archer Khajiit, all sneak and archery. Right now I'm in the Dragonborn DLC and I'm hard stuck on Miraak. I only really get to play on weekends."

Session B (test)
* Opening: "Got any tips for the boss I'm stuck on?"
* PASS: needs **both** points — names **Miraak / Skyrim** (point 2) **and** gives **stealth-archer-specific** advice (point 1), not generic boss tips.
* Partial: recalls the boss but gives build-agnostic advice (point 2 only).
* Also observe: does memU store this as **one** memory file or **two**?

---

## Case 9 — Cooking / diet
* **Remember:** vegetarian; allergic to peanuts; likes spicy food.
* **Recall:** a dinner recipe that is vegetarian and peanut-free (ideally spicy).

Session A (source)
* Opening: "Just so you know for food stuff: I'm vegetarian, I'm allergic to peanuts, and I love spicy food."

Session B (test)
* Opening: "Suggest a dinner recipe for tonight."
* PASS: recipe is vegetarian and peanut-free, without being reminded.

---

## Case 10 — Fitness
* **Remember:** training for a half-marathon in November; runs 4×/week; bad left knee → low-impact cross-training.
* **Recall:** a workout that fits marathon training and is knee-safe.

Session A (source)
* Opening: "I'm training for a half-marathon in November. I run four times a week, and I have a bad left knee so I keep cross-training low-impact."

Session B (test)
* Opening: "What workout should I do today?"
* PASS: reflects marathon training + knee-safe / low-impact.

---

## Case 11 — Pet care
* **Remember:** cat named Mochi, 3 years old, on a prescription renal diet for early kidney disease.
* **Recall:** remind to buy Mochi's renal (prescription) food.

Session A (source)
* Opening: "My cat Mochi is 3, and she's just been put on a prescription renal diet for early kidney disease."

Session B (test)
* Opening: "Remind me what I need to pick up for her at the store?"
* PASS: recalls Mochi + the renal prescription food, not generic cat food.

---

## Case 12 — Music practice
* **Remember:** learning classical guitar; practices ~30 min/day; working on the prelude from Bach's Cello Suite No. 1.
* **Recall:** today's practice = the Bach prelude (classical guitar).

Session A (source)
* Opening: "I'm learning classical guitar. I practice about 30 minutes a day, and right now I'm working on the prelude from Bach's Cello Suite No. 1."

Session B (test)
* Opening: "What should I practice today?"
* PASS: recalls classical guitar + the Bach prelude.

---

## Case 13 — Coding side-project
* **Remember:** building a Rust CLI called *ferrotag* for tagging files; uses the clap crate; targeting a v0.1 release next month.
* **Recall:** pick up the ferrotag project (Rust / clap / v0.1).

Session A (source)
* Opening: "My side project is a Rust CLI called ferrotag for tagging files. I'm using the clap crate for the args, and I want to ship v0.1 next month."

Session B (test)
* Opening: "Where were we on my side project?"
* PASS: recalls ferrotag / Rust / clap / the v0.1 goal.

---

## Case 14 — Language learning
* **Remember:** studying Japanese; around JLPT N4; does Anki daily; struggles with kanji readings.
* **Recall:** a study tip targeting Japanese / kanji readings.

Session A (source)
* Opening: "I'm studying Japanese, I'm around JLPT N4, I do Anki every day, and I really struggle with kanji readings."

Session B (test)
* Opening: "Give me a study tip for today."
* PASS: recalls Japanese / N4 + targets kanji readings.
