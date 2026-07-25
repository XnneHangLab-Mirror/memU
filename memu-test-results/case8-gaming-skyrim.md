# memU recall test — Case 8 (Playing games · Skyrim / Miraak, two remember points)

**Host:** codex-cli 0.144.5 (grok-4.5 via relay) · **Date:** 2026-07-25
**Embedding:** Ollama `bge-m3` · **Store:** isolated `~/.memu-test` (real store never
written) — 3 memories before this case, **5 after**. **Verdict: PASS ✅ (both points)**

**Summary of counts**
- **Memories saved from Session A: 2** — `gaming-skyrim-stealth-archer` (point 1)
  and `gaming-skyrim-miraak-blocker` (point 2). Mined as two separate items so a
  half-recall would show up as *Partial*.
- **Memories recalled in Session B: 3** — both Skyrim memories (ranked #1 and #2)
  **plus one false positive** (`reading-mishima-sea-of-fertility`, #3). See §6.
- Store after commit: **5 memories**.

---

## 1. Session A — source (FULL chat log)
Rollout: `~/.codex/sessions/2026/07/25/rollout-2026-07-25T11-05-21-019f9705-….jsonl`

**USER:**
> I've been playing Skyrim on PC - heavily modded - and I run a stealth-archer Khajiit, all sneak and archery. Right now I'm in the Dragonborn DLC and I'm hard stuck on Miraak. I only really get to play on weekends.

**ASSISTANT (grok-4.5), full text:**
> That fight is brutal for pure stealth archers — Miraak's whole kit punishes "hide and snipe." Here's a weekend-session plan built around sneak + bows.Weekend-friendly game plan for a sneak archer vs Miraak:
>
> ## How the fight works
> Miraak is not a normal boss. At low health he flies off, absorbs a dragon soul, and heals. That happens about **3 times**. You do **not** try to race him to zero in one go. You chip him, survive the phases, then finish him after the last absorption.[[1]](https://www.youtube.com/watch?v=wxJ29vByakA)
>
> Dragons spawn and help him. Use full **Bend Will** (all 3 words) on a dragon so it turns and attacks Miraak. When that dragon dies near him, he absorbs it and you get another phase. Don't dump everything into him while he still has free heals left.[[2]](https://forums.nexusmods.com/topic/930986-dragonborn-miraak-fix-wayaround-console/page/3/)
>
> ## Prep before you go in (one short session)
> Do this on Friday night so Saturday is pure fight time:
>
> - **Shock resistance** — he spams lightning. Stack resist shock gear + potions. This alone fixes a lot of one-shots for light-armor sneak builds.[[3]](https://www.reddit.com/r/skyrim/comments/10lcgyv/how_do_i_kill_miraak_i_fucked_up_by_building_a/)
> - **Health potions + fortify health / restore health** — you're not a tank; buffer the chip damage.
> - **Paralysis / damage health / weakness to poison** on arrows if you use alchemy.
> - **Invisibility potions** (or spell) — core stealth-archer tech for this fight.[[3]]
> - Best bow you have (Nightingale / Auriel's / Dragonbone + enchant/poison).
> - Full **Bend Will**, **Dragon Aspect** if you have it, **Become Ethereal** for panic, **Slow Time** if unlocked.
> - Optional cheese: **Sanguine Rose** or other summons for aggro while you snipe.[[3]]
>
> If you're heavily modded, also check that nothing broke Bend Will, dragon AI, or Miraak's scripts. Script-heavy combat overhauls sometimes make this fight glitchier.
>
> ## Stealth-archer loop (what actually works)
> 1. **Open from stealth** — full sneak multishot / power shot into his back if you can start hidden.
> 2. **Use the arena geometry** — big books/walls/ledges in the center pool area. Pop out, shoot, duck. Stay mobile; don't stand in the open trading spells.[[4]](https://www.youtube.com/watch?v=I6lpPRVNnVA)
> 3. **When he starts nuking you** — crouch + invis, break line of sight, re-sneak, re-open. Level 100 Sneak + invis is the classic archer answer here.[[3]]
> 4. **When a dragon is up** — Bend Will it, let it tank/hit Miraak, keep shooting from cover.
> 5. **After each absorption** — he comes back healed. Reset: invis/sneak, re-apply poison, repeat.
> 6. **Final phase** — no more free heals. Dump DPS: poison, Dragon Aspect, Slow Time, highest-damage arrows.
>
> ## Common stealth-archer failure points
> | Problem | Fix |
> |---|---|
> | Lightning deletes you | Resist shock gear + potions first |
> | Can't re-sneak mid-fight | Invis potions / Quiet Casting / break LOS behind books |
> | Fight never ends | You're not letting dragon phases resolve; use Bend Will, don't only DPS Miraak |
> | Bend Will "does nothing" | All 3 words, clear LOS on the dragon, not mid-animation spam |
> | Out of potions mid-run | Make 20+ invis + heal + resist shock before entering Apocrypha |
>
> ## Khajiit-specific notes
> - Night Eye is useless here; ignore it.
> - Claws don't matter if you're pure bow — stay ranged.
> - High Sneak + Archery is still correct; don't respec into melee for this one fight.
>
> ## Weekend schedule (realistic)
> - **Session 1 (30–45 min):** craft potions, gear check, quicksave outside the Black Book.
> - **Session 2:** 3–5 attempts learning his patterns. Expect deaths; the arena is the tutorial.
> - **Session 3:** clean kill once shock resist + invis loop feels automatic.
>
> If you want, next message can be either:
> 1. a **mod-aware checklist** (what kinds of mods break Miraak), or
> 2. a **shopping/craft list** for potions and enchants tailored to your level/gear,
>
> …or tell me roughly your level, bow, and whether you have Alchemy 100 / Quiet Casting / Dragon Aspect and I'll tighten this into a one-page loadout.

---

## 2. Memories saved (FULL originals, verbatim — 2 files)
`memu-codex commit` → `committed 2 recall file(s) and 0 resource(s)`:
`memory/gaming-skyrim-miraak-blocker`, `memory/gaming-skyrim-stealth-archer`.

### 2a. `gaming-skyrim-stealth-archer` (Remember point 1 — playstyle/setup)
```markdown
---
name: gaming-skyrim-stealth-archer
description: Plays The Elder Scrolls V: Skyrim on PC (heavily modded), running a stealth-archer Khajiit build — sneak, archery, light armour
---

Plays **The Elder Scrolls V: Skyrim** on **PC**, with a **heavily modded** setup.

**Build / playstyle:** runs a **stealth-archer Khajiit** — "all sneak and archery".
Leans on **Sneak** and **Archery** (light-armour, ranged), not melee.

Practical implication for advice: tips should suit a **ranged stealth build**
(sneak openers, invisibility, breaking line of sight, bow/poison damage) rather
than tanky melee play. Being heavily modded also means script-heavy combat
overhauls can affect scripted fights.
```

### 2b. `gaming-skyrim-miraak-blocker` (Remember point 2 — progress/blocker)
```markdown
---
name: gaming-skyrim-miraak-blocker
description: Partway through Skyrim's Dragonborn DLC and hard stuck on the boss Miraak; only gets to play on weekends
---

Currently partway through the **Dragonborn DLC** in **Skyrim**, and is **hard
stuck on Miraak** — this is the active blocker in the playthrough.

**Play schedule:** only really gets to play on **weekends**, so advice should fit
weekend-sized sessions (prep in one short session, attempts in the next).

Context on the fight established while discussing it: Miraak flies off and
absorbs a dragon soul to heal roughly **3 times**, so the fight is about
surviving phases rather than racing his health bar; **Bend Will** on a dragon and
**shock resistance** matter a lot.
```

---

## 3. Retrieval — what Session B recalled (FULL, verbatim)
Exact command the Session B agent ran:
`memu-codex retrieve "game boss tips stuck on boss progress"`
**Recalled: 3 memory files** + 5 segments.

**Segments (5), with scores:**
1. `0.5789` — "stuck on Miraak** — this is the active blocker in the playthrough."
2. `0.5588` — "Practical implication for advice: tips should suit a **ranged stealth build**"
3. `0.5397` — "surviving phases rather than racing his health bar; **Bend Will** on a dragon and"
4. `0.5308` — "Currently partway through the **Dragonborn DLC** in **Skyrim**, and is **hard"
5. `0.5195` — "**Progress / current focus:** about **a third of the way through**; especially"  ← *from the Mishima memory (false positive)*

**File 1 (correct):** `gaming-skyrim-miraak-blocker` · track: memory · score `0.5789`
- **description:** "Partway through Skyrim's Dragonborn DLC and hard stuck on the boss Miraak; only gets to play on weekends"
- **content:**
  ```
  Currently partway through the **Dragonborn DLC** in **Skyrim**, and is **hard
  stuck on Miraak** — this is the active blocker in the playthrough.

  **Play schedule:** only really gets to play on **weekends**, so advice should fit
  weekend-sized sessions (prep in one short session, attempts in the next).

  Context on the fight established while discussing it: Miraak flies off and
  absorbs a dragon soul to heal roughly **3 times**, so the fight is about
  surviving phases rather than racing his health bar; **Bend Will** on a dragon and
  **shock resistance** matter a lot.
  ```

**File 2 (correct):** `gaming-skyrim-stealth-archer` · track: memory · score `0.5588`
- **description:** "Plays The Elder Scrolls V: Skyrim on PC (heavily modded), running a stealth-archer Khajiit build — sneak, archery, light armour"
- **content:**
  ```
  Plays **The Elder Scrolls V: Skyrim** on **PC**, with a **heavily modded** setup.

  **Build / playstyle:** runs a **stealth-archer Khajiit** — "all sneak and archery".
  Leans on **Sneak** and **Archery** (light-armour, ranged), not melee.

  Practical implication for advice: tips should suit a **ranged stealth build**
  (sneak openers, invisibility, breaking line of sight, bow/poison damage) rather
  than tanky melee play. Being heavily modded also means script-heavy combat
  overhauls can affect scripted fights.
  ```

**File 3 (FALSE POSITIVE):** `reading-mishima-sea-of-fertility` · track: memory · score `0.5195`
- **description:** "Reading Runaway Horses by Yukio Mishima (book 2 of the Sea of Fertility tetralogy) — about a third in, following the character Isao; reads a chapter nightly before bed; wants to work through more Mishima this year"
- **content:**
  ```
  Currently reading **Runaway Horses** (奔马) by **Yukio Mishima** — the **second
  novel** in his **Sea of Fertility tetralogy** (丰饶之海四部曲; series order:
  Spring Snow → Runaway Horses → The Temple of Dawn → The Decay of the Angel).
  Really into it.

  **Progress / current focus:** about **a third of the way through**; especially
  taken with the character **Isao (饭沼勋)**, the intense young idealist — at the
  point where he has **just started gathering his group of followers**.

  **Reading habit:** reads **a chapter every night before bed**.

  **Goal for this year:** wants to **work through more of Mishima's writing** — open
  to continuing the tetralogy (next up: *The Temple of Dawn*) and to other Mishima
  works.
  ```
- **resources:** none (all three files)

---

## 4. Session B — test (FULL chat log)
Isolated cwd; **roam/peek hits: 0**; retrieve calls: **3**.
Rollout in `memu-c8-logs/B_rollout.txt`.

**USER:**
> Got any tips for the boss I'm stuck on?

**ASSISTANT (grok-4.5), full text:**
> Yeah — from your progress, this is **Miraak** in Skyrim's Dragonborn DLC, and you're on a **stealth-archer Khajiit**. That fight is mostly about surviving phases, not melting him in one go.
>
> ### Core fight logic
> - He flies off and **absorbs a dragon soul** to heal **~3 times**. Don't panic when his bar fills back up — that's scripted.
> - **Bend Will** a dragon when one shows up. A controlled dragon does real work and eats pressure off you.
> - Bring **shock resistance** (gear, potions, or both). His lightning hurts a lot if you're soft.
>
> ### Stealth-archer game plan
> - Open from stealth with a strong poisoned shot (damage + paralysis or lingering poison if you have it).
> - After he detects you: **kite**, break LOS behind pillars/geometry, re-stealth with **Invisibility** / muffle / sneak potions when you can.
> - Stay at range; don't get sucked into melee. Light armor + distance is your whole identity.
> - Use **slow-time** or similar shout/ability windows to dump damage during vulnerable phases.
> - Keep a stack of:
>   - health/stamina potions
>   - **shock resist** potions
>   - invisibility / fortify sneak / fortify archery
>   - good arrows + poisons
>
> ### Weekend-sized approach
> Since you mostly play weekends:
> 1. **Short prep session:** farm/craft potions, check enchantments (shock resist, fortify archery/sneak), make sure Bend Will is ready, stock poisons.
> 2. **Attempt session:** 2–3 clean tries with saves before the arena, then stop if you're tilted.
>
> ### If it still feels unfair
> Heavy mods can make scripted bosses nastier (combat overhauls, magic overhauls, AI packages). If Miraak's damage or detection feels broken vs vanilla expectations, try:
> - temporarily dialing combat/magic mods down for this fight, or
> - checking whether a mod is interfering with dragon summoning / Bend Will.
>
> If you tell me your level, main bow/enchants, and whether you already have **Bend Will III**, I can tighten this into a more exact loadout checklist.

---

## 5. Verdict — PASS ✅ (both remember points)
The probe named **no game and no boss** — only "the boss I'm stuck on".

| Requirement | Result |
|---|---|
| **Point 2** — names Miraak / Skyrim | ✅ "this is **Miraak** in Skyrim's Dragonborn DLC" |
| **Point 1** — stealth-archer-specific advice | ✅ sneak openers, kite + break LOS, re-stealth with Invisibility, "stay at range… light armor + distance is your whole identity", fortify sneak/archery |
| Not generic boss tips | ✅ build-tailored throughout |
| *Bonus* — weekend schedule (point 2) | ✅ "Weekend-sized approach" — prep session + attempt session |
| *Bonus* — heavily modded (point 1) | ✅ "Heavy mods can make scripted bosses nastier… check whether a mod is interfering with Bend Will" |

Not a Partial: **both** memories were retrieved (ranked #1 and #2) and **both** were
used in the answer. Attribution verified — recall came through `memu-codex retrieve`
with 0 artifact peeking.

---

## 6. Finding — false-positive retrieval from content-free segments
The unrelated **Mishima reading memory was also returned** (rank #3, `0.5195`),
pulled in by the segment:
> "**Progress / current focus:** about **a third of the way through**; especially"

An earlier preview with the literal probe text ("Got any tips for the boss I'm stuck
on?") pulled the same memory via an even emptier segment: **"Really into it."**
(`0.5133`).

**Why it matters:** both are *structurally* generic — a section heading
("Progress / current focus") and a filler sentence — carrying no topical content.
They embed near almost any "what am I in the middle of" query, so they act as
**noisy attractors** and surface unrelated memories. Here it was harmless (the
agent ignored it and the two real memories outranked it), but in a large store
these low-information chunks would crowd out real hits.

**Actionable for memU:** when mining memories, avoid emitting standalone
content-free lines (bare headings, "Really into it.") as their own segments — or
have chunking merge a heading with the text beneath it, so every segment carries
topical signal. This is the first false positive observed across Cases 4, 5, 7,
7.5 and 8, and it appeared only once the store grew past a handful of memories.
