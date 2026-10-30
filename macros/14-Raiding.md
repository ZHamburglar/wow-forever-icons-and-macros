# Raiding Macros — WoW: Forever

The third layer: **raid-specific macros** for organized PvE — leader tools, tank-swap taunts, cooldown stacking, raid CD coordination, and class "raid duty" macros (dispels, interrupts, buffs, curses). All use WotLK-era commands verified against the client's command set.

> [!info] Why this file exists
> Solo/leveling macros optimize *your* gameplay. Raid macros optimize **the group's** — they coordinate cooldowns, automate assignments (who interrupts, who dispels, who marks), and compress panic reactions (tank swap, raid damage, wipe prevention) into one key. In a raid, reaction time is measured in **one second or less** — these macros remove the thinking step.

---

# 📣 Raid Leader Tools

### Ready Check (one key)
```lua
/readycheck
```
> [!tip] Why it's useful
> The built-in `/readycheck` pings every raid member for a Ready/Not-Ready popup. **Why macro it?** Because it belongs on the same key cluster as your pull macros — one hand runs the whole pull sequence without opening menus. Press it before every pull while trash is being cleared.

### Mark Targets (skull / cross / moon)
```lua
#showtooltip
/script SetRaidTarget("target", 8)
```
> [!tip] Why it's useful
> **8 = Skull** (kill first), 7 = X (kill second), 3 = Moon (CC), 4 = Triangle (trap). Marking targets mid-fight is the single biggest DPS-coordination tool in raiding. Script-based marking works on the WotLK-era client and is instant — no menu navigation. Bind three of these (Skull/X/Moon) to Q/E/R.

### Mark Skull + Announce (leader call)
```lua
/script SetRaidTarget("target", 8)
/script SendChatMessage("SKULL -> "..UnitName("target"), "RAID")
```
> [!tip] Why it's useful
> Marks the kill target **and** announces it in raid chat in one press. The `UnitName` pull makes the call self-documenting — no "who's skull?" questions when the pull starts. *(Name callouts to raid chat work on the WotLK-era client.)*

### Assist the Main Tank (pull follower)
```lua
#showtooltip
/assist [@focus,exists]
/startattack
```
> [!tip] Why it's useful
> Sets your focus to the MT at the start of the raid, then this button snaps you onto whatever they're tanking and starts attacking. **Why it matters:** it eliminates the "I attacked the wrong target" problem entirely — your DPS always lands on the tank's current target, which is the correct kill order.

### Tank-Swap Taunt (raid tanking)
```lua
#showtooltip
/cast [@focus,harm,nodead] Taunt; [@mouseover,harm,nodead] Taunt
```
> [!tip] Why it's useful
> In a **tank swap**, the off-tank must taunt the boss the instant the debuff lands. Focus = the boss, one key = instant taunt with zero target-switching. The mouseover fallback lets you grab loose adds (or the other tank's boss) by hovering. This is THE tank macro — it decides wipes vs. clean swaps.

---

# ⚡ Cooldown Coordination (DPS)

### Full Burst (trinkets + racial + potion)
```lua
#showtooltip
/cast Blood Fury
/use 13
/use 14
/use [combat] Potion of Wild Magic
```
> [!tip] Why it's useful
> Raid DPS is measured in **cooldown windows**. This stacks your racial (+attack power/int), both trinkets, and a combat potion into one keypress so they overlap during the boss's damage window (or Heroism/Bloodlust). **Why overlap matters:** multiplicative buffs stacked together produce dramatically more damage than using them spread out. One key = the whole burst.

### Execute-Phase Button (weapon swap + execute)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/cast Execute
```
> [!tip] Why it's useful
> Warriors in raid swap to a 2H for the sub-20% execute phase. This macro does the swap *and* fires Execute in one press. **Why:** boss fights have a defined execute window — every GCD you lose swapping gear manually is a GCD not spent executing. Bind it next to your Execute key.

### Heroism/Bloodlust Caller (shaman)
```lua
#showtooltip
/cast Elemental Mastery
/script SendChatMessage("BURST WINDOW - DPS NOW", "RAID")
```
> [!warning] Bloodlust doesn't exist in Forever
> Classic-era Shaman has **no Bloodlust/Heroism** (added in TBC). The Forever raid-burst call is **Elemental Mastery** (talent): instant, guaranteed-crit, +20% Lightning Bolt. Still announce the window so DPS pop their cooldowns together — that coordination is what makes the burst work.
> [!tip] Why it's useful
> Bloodlust is the raid's biggest damage window — but only if DPS **uses their cooldowns during it**. The announcement makes the window obvious and removes the "should I pop now?" hesitation. One key: lust + call.

---

# 💚 Raid Healing (healer coordination)

### Tank-Assist Heal (heal whoever the boss is hitting)
```lua
#showtooltip
/cast [@targettarget,help,nodead][@mouseover,help,nodead][@player] Flash Heal
```
> [!tip] Why it's useful
> The **tank-heal assist**: target the boss, spam this, and you automatically heal the tank who has aggro. In single-tank fights this is faster than mouseover raid frames — zero targeting overhead. The fallback chain (mouseover → self) keeps it useful everywhere else.

### Dispel Priority Chain (raid dispel duty)
```lua
#showtooltip
/cast [@mouseover,help,nodead] Cleanse; [@focus,help,nodead] Cleanse; [@player] Cleanse
```
> [!tip] Why it's useful
> Raids assign healers to dispel duty (e.g. every 10s on a raid-wide debuff). Mouseover-first means you dispel whoever you're hovering (usually the tank or a raid frame) without dropping your heal target; focus catches the off-tank; self as last resort. **Why priority chains:** in a dispel rotation there's no time to retarget — the macro picks the right person for you.

### Raid CD: Save the Tank (priest/druid/paladin)
```lua
#showtooltip
/cast [@focus,help,nodead] Power Word: Shield; [@mouseover,help,nodead] Power Word: Shield
```
> [!tip] Why it's useful
> **Guardian Spirit doesn't exist in Forever** (WotLK-era). The classic-era tank-save is a pre-cast **Power Word: Shield** on the tank you're assigned to protect — focus = tank, one key fires the bubble when the boss's big hit lands. Paladins use **Blessing of Sacrifice**, druids use **Innervate→heal** or pre-HoT Rejuvenation. The pattern holds: pre-assigned focus + one key = no target-switching during a 1-second tank-buster.

### Mana Regen Trio (pot + innervate + shadowfiend)
```lua
#showtooltip
/use [combat] Major Mana Potion
/cast [@player] Innervate
```
> [!tip] Why it's useful
> Long boss fights are mana marathons. This combines your mana pot with your personal mana-regen CD (Innervate for druids — **Shadowfiend doesn't exist in Forever**, it's WotLK-era). **Why combine:** you only have one potion per fight — timing it with your regen CD stretches both further. *(Non-druids: swap the second line for your own regen tool, e.g. Mage's Evocation.)*

---

# 🛡️ Tank Survival (raid tanking)

### Emergency Tank CD (all defensives)
```lua
#showtooltip
/cast Shield Wall
/cast Last Stand
/use [combat] Indestructible Potion
```
> [!tip] Why it's useful
> The **oh-shit button** for tanking: damage reduction + max-HP boost + defensive potion in one press. **Why:** raid bosses hit for 20-30k in WotLK-era gear — a tank has ~2 seconds to react to a bad debuff stack. Three separate keys = death. One key = survival. *(Every tank class has an equivalent: Shield Wall, Divine Shield, Survival Instincts, Icebound Fortitude.)*

### Add Taunt (pick up loose mobs)
```lua
#showtooltip
/cast [@mouseover,harm,nodead] Growl; [harm] Growl
```
> [!tip] Why it's useful
> Adds spawning behind the raid need taunting **yesterday**. Mouseover-taunt lets you grab the add without changing your boss target (and losing your tank rotation position). **Why mouseover:** you stay on the boss the whole time — the add is grabbed by hovering, not targeting.

### Threat Opener (sunder/maul/righteous fury + attack)
```lua
#showtooltip
/startattack
/castsequence reset=target Sunder Armor, Sunder Armor, Sunder Armor, Sunder Armor, Sunder Armor
```
> [!tip] Why it's useful
> A tank who loses aggro on pull wipes DPS. This builds a full 5-stack armor shred + threat instantly and **auto-resets on target change** — the pull opener is always correct, every time. **Why sequence:** it removes "which stack am I on?" from your brain during the chaotic first 10 seconds.

---

# 🎯 Raid Duty Macros (class assignments)

### Interrupt Duty (focus + mouseover + target)
```lua
#showtooltip
/cast [@focus,harm,nodead] Kick; [@mouseover,harm,nodead] Kick; [harm] Kick
```
> [!tip] Why it's useful
> Raids assign 2-3 interrupters to a boss cast (e.g. every 8s). Your focus = the boss, so this always interrupts the assigned target; mouseover catches adds; target is the fallback. **Why:** a missed interrupt on a raid boss = raid-wide damage or wipe. The chain guarantees your interrupt lands on the right cast every time.

### Dispel/Steal Duty (mage Remove Lesser Curse)
```lua
#showtooltip
/cast [@focus,harm,nodead] Remove Lesser Curse; [@mouseover,harm,nodead] Remove Lesser Curse
```
> [!tip] Why it's useful
> Some bosses put **curses** on the raid that must be stripped on cooldown. **Spellsteal doesn't exist in Forever** (TBC+) — the mage's assigned duty is **Remove Lesser Curse**. Focus-based keeps the rotation automatic — you keep DPSing the boss and the cleanse happens with one key. **Why focus:** it's the same boss every time — why retarget it?

### Warlock Curse Duty (elements/weakness)
```lua
#showtooltip
/cast [mod:shift] Curse of Weakness; Curse of the Elements
```
> [!tip] Why it's useful
> Raids need specific curses up at all times (Elements for spell damage, Weakness for physical). One key keeps your assigned curse applied; shift swaps to the secondary. **Why:** curse uptime is a flat raid-DPS multiplier — a forgotten curse is lost damage every second it's down.

### Hunter Burst on Tank (threat control)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Bestial Wrath
/petattack
```
> [!tip] Why it's useful
> **Misdirection doesn't exist in Forever** (TBC+). The classic hunter threat control is pacing: use **Bestial Wrath** (talent) + pet attack timing instead of MD. Focus = the kill target, one key = pet burst + send-in. Hunters still do their biggest damage in the first 15 seconds (trap + opener burst) — use the window, watch threat.

### Battle Rez Duty (druid)
```lua
#showtooltip
/cast [@mouseover,dead] Rebirth; [@target,dead] Rebirth
```
> [!tip] Why it's useful
> Combat rezzes are a limited raid resource. This targets a dead raid member by mouseover (or current dead target) and rezzes them instantly. **Why:** during a boss fight, the seconds a DPS spends dead are lost raid DPS; a dead tank is a wipe. The macro removes the "find the corpse in the raid frame" step.

---

## 📋 Raid Macro Quick Reference

| Role | Macro | Key Insight |
|---|---|---|
| Leader | `/readycheck` + mark scripts | Whole pull sequence on one hand |
| DPS | Full burst stack | Overlap cooldowns = multiplicative damage |
| Healer | Tank-assist heal | Heal whoever the boss hits |
| Healer | Dispel priority chain | No retargeting in dispel rotations |
| Tank | Tank-swap taunt | Focus-based = correct tank every swap |
| Tank | Emergency CD button | 2-second reaction = one key |
| Interrupter | Focus interrupt chain | Never miss the assigned cast |
| Support | curse duty / pet burst | Automation beats assignment memory |

---

> [!note] Raid addons
> WotLK-era raid frames + DBM/BigWigs handle timers; these macros handle **actions**. If your Forever client supports addons, pair these with DBM for pull timers — if not (beta client), `/readycheck` + the announce macros above replace the pull-timer role.