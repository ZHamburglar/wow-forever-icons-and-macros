# Warrior Macros — WoW: Forever

Stance dancing, Charge/Intercept combos, weapon swapping, and Execute smashing. Classic-era Warrior (level 60) with 3 stances.

> [!tip] Stance IDs
> `[stance:1]` = Battle, `[stance:2]` = Defensive, `[stance:3]` = Berserker

> [!tip] Weapon slots
> 16 = main hand, 17 = off hand. Weapon names in these macros are placeholders — **swap in your actual gear**.

---

## ⚔️ Rotation & Damage

### Charge + Rend (opener)
```lua
#showtooltip
/cast [stance:1] Charge; [stance:3] Intercept
/cast Rend
```
*(Battle stance → Charge, Berserker → Intercept, then Rend)*

> [!tip] Why it's valuable
> One key handles the stance check - Charge from Battle, Intercept from Berserker - and lands Rend on arrival, so the opener's gap-close and bleed fire in a single press.

### Mortal Strike + Auto-Attack
```lua
#showtooltip
/startattack
/cast [stance:1] Mortal Strike
```

> [!tip] Why it's valuable
> /startattack gets the swing going before Mortal Strike lands so no GCD is wasted, and [stance:1] prevents dead presses outside Battle stance.

### Whirlwind (Berserker stance auto-switch)
```lua
#showtooltip
/cast [stance:3] Whirlwind
```

> [!tip] Why it's valuable
> [stance:3] makes the button safe to hammer - it only fires in Berserker stance, and one key covers your AoE burst on every pack.

### Execute (any stance)
```lua
#showtooltip
/cast Execute
/startattack
```

> [!tip] Why it's valuable
> Execute works from any stance, so the finisher fires the instant the target drops below 20% health - no stance dance between you and the kill.

### Execute Weapon-Swap (big 2H for the finisher)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/cast Execute
```
> [!tip] Why it's valuable
> **Execute's damage scales with weapon max-damage** in Classic-era combat math — a slow, high-top-end 2H makes every Execute hit dramatically harder than your fast 1H. This macro swaps to the big stick *and* fires Execute in one press. **Why it matters:** the sub-20% execute phase is where warrior DPS goes vertical — this is the button that makes the last 20% of the boss your best 20%.
>
> **Advanced timing trick:** every weapon swap **resets your swing timer**, a free DPS gain — so press this on the execute-phase GCD, then hit **Swap Back** below to restore your normal set and start the next auto-swing fresh. *(The swap-back is a separate key because `/castsequence` chokes on item names containing commas — the comma is its step separator. Two buttons, zero broken sequences.)*

### Swap Back (return to your normal weapons)
```lua
#showtooltip
/equipslot 16, Sword of the Twin Blades
/equipslot 17, Bulwark of Azzinoth
```
> [!tip] Why it's valuable
> The **second half of the dance**: after the Execute swap, this restores your normal weapon set — and the swap resets the swing timer *again*, so the whole cycle (big hit → swap → fresh swing) is a net DPS gain. Bind it right next to the Execute button and train the rhythm: Execute → swap-back → continue rotation.

### Overpower (proc watcher)
```lua
#showtooltip
/cast [stance:1] Overpower
```

> [!tip] Why it's valuable
> Turns every enemy dodge into a guaranteed crit - one press the moment the proc lights up, with no stance-bar hunting mid-fight.

### Overpower Dance (proc → Battle → hit)
```lua
#showtooltip
/cast [stance:1] Overpower; Battle Stance
```
> [!tip] Why it's valuable
> **Overpower only fires from Battle Stance** — and only after your target dodges. The "dance": when the proc shows up, press once to stance into Battle (if needed), press again to Overpower. Two presses total, zero stance-hunting. The payoff: a **guaranteed crit** on a free swing every time your target dodges.

### Overpower Big-Weapon (swap in a slow 2H for the proc)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/cast [stance:1] Overpower; Battle Stance
```
> [!tip] Why it's valuable
> Overpower crits are **weapon-damage based** — the same trick as Execute: swap to the big 2H, stance-dance into Battle, land the free crit, and the swing-timer reset means you don't lose your next auto. One macro, three things happening in the right order.

### Slam (no cast bar cancel)
```lua
#showtooltip
/stopcasting
/cast Slam
```

> [!tip] Why it's valuable
> One key fires Slam and uses /stopcasting to snap out of whatever you were mid-cast on - the classic fake-cast control that baits interrupts or clips the swing at the perfect moment.

### Slam Cancel-Cast (big weapon + no-castbar)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/cast [stance:1] Slam; Battle Stance
/stopcasting
```
> [!tip] Why it's valuable
> **Slam is a cast-time attack** whose damage uses your weapon — so the slow 2H maximizes it. The `stopcasting` line is the classic trick: Slam's cast bar can be cancelled to fake-cast and bait interrupts (you keep rage), or to clip it at the perfect moment. One key: big weapon, right stance, cancel control.

### Thunder Clap + Demo Shout (AoE threat)
```lua
#showtooltip
/cast [stance:2] Thunder Clap
/cast Demoralizing Shout
```

> [!tip] Why it's valuable
> AoE damage and the attack-power debuff stack on one key - [stance:2] keeps Thunder Clap honest while Demoralizing Shout lands from any stance, a one-press AoE threat package.

---

## 🛡️ Tanking (Protection)

### Shield Slam (Defensive auto-switch)
```lua
#showtooltip
/cast [stance:2] Shield Slam
/startattack
```

> [!tip] Why it's valuable
> [stance:2] means the button only fires in Defensive stance, and /startattack keeps the swing rolling - your highest single-target threat with no dead presses.

### Taunt Macro — mouseover or focus
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Taunt
```

> [!tip] Why it's valuable
> Resolves three priorities in one press - mouseover, then focus, then current target - the difference between catching the add and watching the healer die.

### Taunt + Defensive (oh-@#$% tank button)
```lua
#showtooltip
/cast [stance:2] Taunt; [nostance:2] Defensive Stance
```
> [!tip] Why it's valuable
> **Taunt requires Defensive Stance** — and the moment you need it is usually *right now* (an add ripped to the healer). One press: if you're not in Defensive, it stances you in; press again and the taunt lands. Two presses beats fumbling the stance bar while the healer dies.

### Shield Block + Shield Bash (interrupt)
```lua
#showtooltip
/cast Shield Block
/cast [stance:2] Shield Bash
```

> [!tip] Why it's valuable
> Block comes up for the incoming melee while Bash stays ready on the same key - one bind covers mitigation plus the interrupt you will need the moment a caster starts channeling.

### Shield Block + Shield Bash (defensive interrupt combo)
```lua
#showtooltip
/cast [stance:2] Shield Block; [stance:2] Shield Bash; [nostance:2] Defensive Stance
```
> [!tip] Why it's valuable
> **Shield Block and Shield Bash are both Defensive-locked.** This macro stance-dances you in and fires the block (for the incoming melee) while keeping Bash ready on the same button — press it when a caster starts channeling and you get the interrupt *and* the mitigation in the same stance dance.

### Spell Reflection (survival)
```lua
#showtooltip
/cast [stance:2] Shield Block
/cast [stance:2] Disarm
```
> [!warning] Spell Reflection removed
> Spell Reflection doesn't exist in Forever (Classic-era Warrior). Use **Shield Block + Disarm** in Defensive stance as the anti-melee defensive instead.

### Last Stand + Shield Wall emergency
```lua
#showtooltip
/cast Last Stand
/cast Shield Wall
```

> [!tip] Why it's valuable
> Pops both survival cooldowns in a single press - the extra health and damage reduction land together exactly when the tank is about to eat a big hit.

### Panic: Defensive + Shield + Last Stand (tank save)
```lua
#showtooltip
/cast [stance:2] Last Stand; [nostance:2] Defensive Stance
/equipslot [mod:shift] 16, Bulwark of Azzinoth
```
> [!tip] Why it's valuable
> The **"I'm about to die" button**: stance into Defensive, pop Last Stand (+30% max HP for 20s — heals you for the gain), and Shift-press to also grab the shield. Raid tanks bind this to a panic key so the save is *one* keystroke, not three. **Why:** when the boss is about to hit you for 90% of your HP, you don't have time for a macro that needs two presses.

### Two-Hander / Sword-and-Board (DPS ↔ tank swap)
```lua
#showtooltip
/equipslot [mod:shift] 16, Sword of the Twin Blades
/equipslot [mod:shift] 17, Bulwark of Azzinoth
/equipslot [nomod] 16, Sulfuras, the Extinguished Hand
```
> [!tip] Why it's valuable
> The **core weapon swap**: Shift = 1H + shield (tank mode: Taunt, Shield Block, Shield Slam), plain = big 2H (DPS mode: Mortal Strike, Execute, Whirlwind). One key swaps your whole threat profile. **Why it matters:** a Warrior that can flip between tanking and DPS *mid-fight* is the difference between a pug that wipes on adds and one that survives. *(Swap in your real weapon names.)*

---

## 🧨 Burst & Cooldowns

### Recklessness + Death Wish (big burst)
```lua
#showtooltip
/cast Recklessness
/cast Death Wish
```

> [!tip] Why it's valuable
> Both damage cooldowns fire on one key - the crit burst and bonus damage share a bind, so your kill window starts the instant you press it.

### Bloodrage + Berserker Rage (rage engine)
```lua
#showtooltip
/cast Bloodrage
/cast Berserker Rage
```

> [!tip] Why it's valuable
> Guarantees starting rage and fear immunity in one press - open every pull with the rage you need and shrug off fears mid-fight.

### Retaliation (parry everything)
```lua
#showtooltip
/cast Retaliation
```

> [!tip] Why it's valuable
> One press parries all melee for 15 seconds - the anti-melee panic button that turns a swarming pack into free counter-attacks.

### Victory Rush self-heal
```lua
#showtooltip
/cast [@player] Victory Rush
```

> [!tip] Why it's valuable
> [@player] guarantees the heal lands on you, not a mouseover - an instant self-top-up the moment a finishing blow procs it.

---

## 🧊 Utility & Control

### Charge / Intercept (one key, both gap-closers)
```lua
#showtooltip
/cast [stance:1] Charge; [stance:3] Intercept; [nostance:1,nostance:3] Battle Stance
```
> [!tip] Why it's valuable
> Warriors have **two gap-closers locked to different stances** — Charge (Battle) for the opener, Intercept (Berserker) for mid-fight re-engages. This one key does the right one from the right stance, and if you're in Defensive it stances into Battle so Charge works. One button, never dead.

### Charge Opener (2H + Battle + Charge + Rend)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
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

### Hamstring (slow kiting)
```lua
#showtooltip
/cast Hamstring
/startattack
```

> [!tip] Why it's valuable
> Slows your current target and starts attacking in the same press - no target juggling when a fleeing enemy is one step from casting range.

### Piercing Howl (AoE slow)
```lua
#showtooltip
/cast Piercing Howl
```

> [!tip] Why it's valuable
> Slows every enemy within 10 yards with no target required - the kiting and peeling button that works even when you are surrounded.

### Intimidating Shout (fear)
```lua
#showtooltip
/cast Intimidating Shout
```

> [!tip] Why it's valuable
> AoE fear on one key gives you breathing room when the pack closes in - enemies flee for up to 8 seconds while you reposition or bandage.

### Mocking Blow (off-tank taunt)
```lua
#showtooltip
/cast [stance:1] Mocking Blow
```

> [!tip] Why it's valuable
> A second taunt that works from Battle stance - off-tanks get a backup threat button without having to stance into Defensive first.

### Stance-Dance (Battle → Defensive → back)
```lua
#showtooltip
/cast [stance:1] Defensive Stance; [stance:2] Battle Stance; [stance:3] Battle Stance
```
*(One button: always returns to Battle stance from any)*

> [!tip] Why it's valuable
> One button returns you to Battle stance from any stance - with Tactical Mastery you keep your rage through the change, making recovery a single keystroke.

### Defensive → Battle → Berserker cycle (utility stances)
```lua
#showtooltip
/cast [stance:2] Battle Stance; [stance:1] Berserker Stance; [stance:3] Battle Stance
```
> [!tip] Why it's valuable
> A **stance cycler** for when you need a specific stance *now*: press from Defensive → Battle (to Charge/Overpower), press again → Berserker (to Intercept/Whirlwind), press again → Battle. With **Tactical Mastery** you keep your rage through the dance — every press is a valid stance change, never a dead button.

### Berserker Stance (for Intercept/Whirlwind)
```lua
#showtooltip
/cast [stance:3] Berserker Stance
```

> [!tip] Why it's valuable
> One key plants you in Berserker stance so Intercept and Whirlwind are live - no stance-bar clicking when the fight heats up.

### Charge + Taunt (pull combo)
```lua
#showtooltip
/cast Charge
/cast Taunt
```

> [!tip] Why it's valuable
> Charge closes the gap and Taunt snaps the pull onto you in one press - the tank opener that secures threat before the group can rip it away.

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Mortal Strike | Main damage |
| 2 | Overpower Dance | Proc + stance |
| 3 | Execute Weapon-Swap | Finisher with big 2H |
| 4 | Whirlwind | AoE |
| Q | Charge/Intercept | Gap closer |
| E | Intimidating Shout | Emergency CC |
| R | Hamstring | Slow |
| F | 2H / Sword-and-Board | Tank↔DPS swap |
| Shift-F | Swap Back | Restore weapons |
| G | Panic: Last Stand + Shield | Tank save |
| Shift-1 | Recklessness + Death Wish | Burst |
| Mouse4 | Stance Dance | Mobility |

---

> [!note] Custom server check
> If a custom talent renamed any ability (e.g. a new finisher), open your Spellbook and use the exact name. The `#showtooltip` will show you what's actually bound. Weapon names are **placeholders — swap in your actual gear**.