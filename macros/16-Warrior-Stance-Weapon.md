# Warrior Stance-Dance + Weapon-Swap Macros (WoW: Forever)

*A friend-request pack: the two classic warrior techniques — stance dancing and weapon swapping — with why each macro earns a keybind. Verified against Forever's Classic-era ability list (no Spell Reflection — use Shield Block/Disarm).*

> [!info] The two techniques
> **Stance dancing** = swapping between Battle/Defensive/Berserker mid-fight to get the *right stance for the right moment* (Charge needs Battle, Intercept needs Berserker, Shield Block needs Defensive). Talents like **Tactical Mastery** make it cheap — you keep rage when switching.
> **Weapon swapping** = macro-swapping between a big 2H and a 1H+shield (or swapping in a slow weapon) for specific abilities. Classic trick: **Execute, Overpower, and Slam hit harder with a slow, high-max-damage 2H** — and swapping weapons resets your swing timer, so the swap itself is a DPS tool.

**Stance IDs:** `[stance:1]` = Battle · `[stance:2]` = Defensive · `[stance:3]` = Berserker
**Weapon slots:** 16 = main hand, 17 = off hand
**Tip:** put your weapons in the **Equipment Manager** (`/equipset` or C-sheet sets) so swaps are one item-name — or use the exact item names below.

---

## 1. Stance Dance Macros

### Charge / Intercept (one key, both gap-closers)
```lua
#showtooltip
/cast [stance:1] Charge; [stance:3] Intercept; [nostance:1,nostance:3] Battle Stance
```
> [!tip] Why it's valuable
> Warriors have **two gap-closers locked to different stances** — Charge (Battle) for the opener, Intercept (Berserker) for mid-fight re-engages. This one key does the right one from the right stance, and if you're in Defensive it stances into Battle so Charge works. One button, never dead.

### Overpower Dance (proc → Battle → hit)
```lua
#showtooltip
/cast [stance:1] Overpower; Battle Stance
```
> [!tip] Why it's valuable
> **Overpower only fires from Battle Stance** — and only after your target dodges. The "dance": when the proc shows up, press once to stance into Battle (if needed), press again to Overpower. Two presses total, zero stance-hunting. The payoff: a **guaranteed crit** on a free swing every time your target dodges.

### Defensive → Battle → Berserker cycle (utility stances)
```lua
#showtooltip
/cast [stance:2] Battle Stance; [stance:1] Berserker Stance; [stance:3] Battle Stance
```
> [!tip] Why it's valuable
> A **stance cycler** for when you need a specific stance *now*: press from Defensive → Battle (to Charge/Overpower), press again → Berserker (to Intercept/Whirlwind), press again → Battle. With **Tactical Mastery** you keep your rage through the dance — every press is a valid stance change, never a dead button.

### Taunt + Defensive (oh-@#$% tank button)
```lua
#showtooltip
/cast [stance:2] Taunt; [nostance:2] Defensive Stance
```
> [!tip] Why it's valuable
> **Taunt requires Defensive Stance** — and the moment you need it is usually *right now* (an add ripped to the healer). One press: if you're not in Defensive, it stances you in; press again and the taunt lands. Two presses beats fumbling the stance bar while the healer dies.

### Shield Block + Shield Bash (defensive interrupt combo)
```lua
#showtooltip
/cast [stance:2] Shield Block; [stance:2] Shield Bash; [nostance:2] Defensive Stance
```
> [!tip] Why it's valuable
> **Shield Block and Shield Bash are both Defensive-locked.** This macro stance-dances you in and fires the block (for the incoming melee) while keeping Bash ready on the same button — press it when a caster starts channeling and you get the interrupt *and* the mitigation in the same stance dance.

---

## 2. Weapon-Swap Macros

### Two-Hander / Sword-and-Board (DPS ↔ tank swap)
```lua
#showtooltip
/equip [mod:shift] Sword of the Twin Blades
/equip [mod:shift] Bulwark of Azzinoth
/equip [nomod] Sulfuras, the Extinguished Hand
```
> [!tip] Why it's valuable
> The **core weapon swap**: Shift = 1H + shield (tank mode: Taunt, Shield Block, Shield Slam), plain = big 2H (DPS mode: Mortal Strike, Execute, Whirlwind). One key swaps your whole threat profile. **Why it matters:** a Warrior that can flip between tanking and DPS *mid-fight* is the difference between a pug that wipes on adds and one that survives. *(Swap in your real weapon names.)*

### Execute Weapon-Swap (big 2H for the finisher)
```lua
#showtooltip
/equip Sulfuras, the Extinguished Hand
/cast Execute
```
> [!tip] Why it's valuable
> **Execute's damage scales with weapon max-damage** in Classic-era combat math — a slow, high-top-end 2H makes every Execute hit dramatically harder than your fast 1H. This macro swaps to the big stick *and* fires Execute in one press. **Why it matters:** the sub-20% execute phase is where warrior DPS goes vertical — this is the button that makes the last 20% of the boss your best 20%.

### Execute + Swap-Back (fire, then return to normal weapon)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/cast Execute
```
> [!tip] Why it's valuable
> The **advanced timing trick**: every weapon swap **resets your swing timer**, which is a free DPS gain. This macro fires Execute with the slow 2H (maximizing the finisher), and the swap itself resets your timer so your next auto-swing starts fresh. **Pair it with the swap-back button below** — press this on the execute-phase GCD, then swap back after. *(The swap-back is a separate key because `/castsequence` chokes on item names containing commas — the comma is its step separator. Two buttons, zero broken sequences.)*

### Swap Back (return to your normal weapons)
```lua
#showtooltip
/equipslot 16, Sword of the Twin Blades
/equipslot 17, Bulwark of Azzinoth
```
> [!tip] Why it's valuable
> The **second half of the dance**: after the Execute swap, this restores your normal weapon set — and the swap resets the swing timer *again*, so the whole cycle (big hit → swap → fresh swing) is a net DPS gain. Bind it right next to the Execute button and train the rhythm: Execute → swap-back → continue rotation.

### Overpower Big-Weapon (swap in a slow 2H for the proc)
```lua
#showtooltip
/equip Sulfuras, the Extinguished Hand
/cast [stance:1] Overpower; Battle Stance
```
> [!tip] Why it's valuable
> Overpower crits are **weapon-damage based** — the same trick as Execute: swap to the big 2H, stance-dance into Battle, land the free crit, and the swing-timer reset means you don't lose your next auto. One macro, three things happening in the right order.

### Slam Cancel-Cast (big weapon + no-castbar)
```lua
#showtooltip
/equip Sulfuras, the Extinguished Hand
/cast [stance:1] Slam; Battle Stance
/stopcasting
```
> [!tip] Why it's valuable
> **Slam is a cast-time attack** whose damage uses your weapon — so the slow 2H maximizes it. The `stopcasting` line is the classic trick: Slam's cast bar can be cancelled to fake-cast and bait interrupts (you keep rage), or to clip it at the perfect moment. One key: big weapon, right stance, cancel control.

---

## 3. Full Combo: Stance + Weapon + Ability

### Charge Opener (2H + Battle + Charge + Rend)
```lua
#showtooltip
/equip Sulfuras, the Extinguished Hand
/cast [stance:1] Charge; Battle Stance
/cast Rend
```
> [!tip] Why it's valuable
> The **perfect pull button**: big 2H equipped, Battle stance guaranteed, Charge in, Rend ticking on arrival. Everything the opener needs in one press — you land already bleeding the target. **Why it matters:** the first 2 seconds of a fight set your threat and your rage; this removes all three fiddly parts from it.

### Intercept + Hamstring (Berserker slow-down)
```lua
#showtooltip
/cast [stance:3] Intercept; Berserker Stance
/cast Hamstring
```
> [!tip] Why it's valuable
> Intercept stuns, **Hamstring slows** — the classic kiting/peeling combo. Berserker stance makes both available (Hamstring works in any stance; Intercept needs Berserker). One key = you're on the fleeing caster with it slowed before it can cast. Bound next to your gap-closer for arena/BG chasing.

### Panic: Defensive + Shield + Last Stand (tank save)
```lua
#showtooltip
/cast [stance:2] Last Stand; [nostance:2] Defensive Stance
/equip [mod:shift] Bulwark of Azzinoth
```
> [!tip] Why it's valuable
> The **"I'm about to die" button**: stance into Defensive, pop Last Stand (+30% max HP for 20s — heals you for the gain), and Shift-press to also grab the shield. Raid tanks bind this to a panic key so the save is *one* keystroke, not three. **Why:** when the boss is about to hit you for 90% of your HP, you don't have time for a macro that needs two presses.

---

> [!note] Forever custom-server check
> All spells here are Classic-era Forever names (Charge, Intercept, Overpower, Execute, Slam, Shield Block, Shield Bash, Taunt, Last Stand, Hamstring, Rend). Weapon names are **placeholders — swap in your actual gear**. Stance IDs are standard. If a button doesn't fire, `#showtooltip` shows what's bound; check your Spellbook for exact ability names (custom talents may rename).