# Druid Macros — WoW: Forever

Form shifting, mouseover HoTs, the classic cat/bear/travel swap, plus the advanced raid toolkit (Lacerate stacking, Rake/Shred CP windows, Hurricane AoE, Swiftmend saves). Classic-era Druid (level 60) — the server's signature class (the leveling guide is built around it).

> [!tip] Form IDs (Druid)
> `[stance:1]` = Bear, `[stance:2]` = Aquatic, `[stance:3]` = Cat, `[stance:4]` = Travel, `[stance:5]` = Moonkin/Boomkin

---

## 🐻🐱 Form Management

### Bear Form (tank)
```lua
#showtooltip
/cast [nostance:1] Bear Form
```


> [!tip] Why it's valuable
> The druid's tank form — huge armor multiplier, rage-based threat. Every feral-tank pull starts here; the nostance guard means the key never double-fires.

### Cat Form (DPS/stealth)
```lua
#showtooltip
/cast [nostance:3] Cat Form
```


> [!tip] Why it's valuable
> The feral DPS form — energy-based CP builders and stealth access. One key from any form; the nostance guard makes it idempotent.

### Travel Form (mount speed)
```lua
#showtooltip
/cast [nostance:4] Travel Form
```


> [!tip] Why it's valuable
> Instant mount-speed travel form that works indoors — the druid's 'always be moving' key. Nostance guard: never wastes a press.

### Aquatic Form (swim fast)
```lua
#showtooltip
/cast [nostance:2] Aquatic Form
```


> [!tip] Why it's valuable
> Fast swimming with underwater breathing — the water-zone traversal key. Nostance guard keeps it safe to spam.

### Moonkin Form (ranged DPS)
```lua
#showtooltip
/cast [nostance:5] Moonkin Form
```


> [!tip] Why it's valuable
> The balance DPS form — +crit aura and caster armor. One key from any form; the guard prevents accidental double-shifts.

### Dire Bear Form (tankier bear — level 40)
```lua
#showtooltip
/cast [nostance:1] Dire Bear Form
```
> [!warning] Flight Form removed
> Flight Form (TBC+) doesn't exist on Forever — no flying at level 60. Dire Bear Form (40) is the classic upgrade to Bear Form: more armor, more threat, same stance 1.

### One-Button Form Switcher (cat/bear/travel)
```lua
#showtooltip
/cast [mod:shift] Bear Form; [mod:ctrl] Cat Form; [mod:alt] Travel Form; [nocombat] Travel Form; [combat] Cat Form
```
*(Shift=Bear, Ctrl=Cat, Alt=Travel — default: Travel out of combat, Cat in combat)*


> [!tip] Why it's valuable
> Four forms on one key via modifiers — Shift=Bear, Ctrl=Cat, Alt=Travel, default = Travel out of combat / Cat in combat. The 'never open your spellbook for a form' button.

### Shift-to-Heal-and-Back (powerful!)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast [stance:3] Healing Touch
```
> [!tip] Shift-heal macro
> Press once in cat → shifts to caster and starts Healing Touch. This is the core leveling heal — the guide uses exactly this pattern.

### Cancel Form (return to caster)
```lua
#showtooltip
/cast [stance:1] Bear Form; [stance:3] Cat Form; [stance:5] Moonkin Form
```
*(Press in any form → drops back to caster form)*


> [!tip] Why it's valuable
> Drops any form back to caster instantly — needed for casting heals, Rebirth, or using items. The druid's most-pressed quality-of-life key after forms themselves.

### Travel + Stealth (stealth travel)
```lua
#showtooltip
/cast [nocombat] Cat Form
/cast [nocombat] Prowl
```
> [!tip] Why it's valuable
> Out of combat: cat form + stealth = **fast movement while stealthed** — the druid's "stealth travel" for crossing hostile territory or scouting a boss room. **Why valuable:** nobody sees you, you move fast, and you're ready to Ravage-opener anything that aggros. One key, zero risk.

### Root-Escape (Entangling Roots + travel)
```lua
#showtooltip
/cast [@focus,harm,nodead] Entangling Roots; [@mouseover,harm,nodead] Entangling Roots
/cast [mod:shift] Travel Form
```
> [!tip] Why it's valuable
> Roots your chaser (focus/mouseover) and, with Shift, hops to travel form to run away — the druid's kiting escape. **Why valuable:** roots don't break on damage-free movement, so you can heal/run while they're stuck. Shift+travel makes the escape complete.

---

## 🌿 Restoration Healing (mouseover)

### Rejuvenation (HoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Rejuvenation
```


> [!tip] Why it's valuable
> The druid's core HoT — mouseover-first means you heal raid frames without changing target. Cheap, instant, and the backbone of resto healing.

### Regrowth (direct + HoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Regrowth
```


> [!tip] Why it's valuable
> Direct heal + HoT in one cast — the resto workhorse. Mouseover keeps it on the tank while your target stays on the boss.

### Healing Touch (big heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Healing Touch
```


> [!tip] Why it's valuable
> The druid's biggest direct heal — slow cast, huge output. Mouseover-first so it lands on whoever you hover in raid frames.

### Swiftmend (talent — consume HoT for instant)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Swiftmend
```
> [!tip] Why it's valuable
> Swiftmend consumes a Rejuvenation or Regrowth on the target for an **instant, huge heal** — the resto druid's emergency save. Mouseover-first means you can rescue anyone in the raid frames without changing your main healing target. **Why valuable:** it's instant, it's big, and it's your only true "oh no" button besides Tranquility.

### Revive (out-of-combat rez — mouseover)
```lua
#showtooltip
/cast [@mouseover,dead] Revive; [@target,dead] Revive
```
> [!warning] Lifebloom removed
> Lifebloom (TBC+) doesn't exist on Forever — classic HoTs are Rejuvenation and Regrowth. Revive is the classic out-of-combat rez; keep the raid rez (Rebirth) for combat.

### Wild Growth (talent — party HoT)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Wild Growth
```


> [!tip] Why it's valuable
> Party-wide HoT in one cast — the resto raid tool for group-wide damage. Talent-gated: greys out until you spend Restoration points.

### Tranquility (channel AoE heal)
```lua
#showtooltip
/cast Tranquility
```
> [!tip] Why it's valuable
> **Tranquility is the resto druid's raid-wide emergency heal** — a channeled AoE that heals the whole party every 2s for 10s. **Why valuable:** it's the classic answer to raid-wide damage spikes; on bosses with predictable bursts, pre-casting it turns a wipe into a save. *(Tree of Life is TBC+ and doesn't exist on Forever — classic resto heals from caster form.)*

### Innervate (mana regen — self or the right healer)
```lua
#showtooltip
/cast [@focus,help,nodead] Innervate; [@mouseover,help,nodead] Innervate; [@player] Innervate
```
> [!tip] Why it's valuable
> Innervate restores a **huge chunk of mana over 20s** — on a raid boss that lasts 8 minutes, the difference between "healer out of mana at 60%" and "healer still casting at 100%" is Innervate placement. Set your focus to the mana-hungry healer (priest/shaman), one key gifts them the mana. **Why valuable:** you're not always the best Innervate target — the raid's throughput healer is. This macro makes it one key.

### Rebirth (combat rez — mouseover + announce)
```lua
#showtooltip
/cast [@mouseover,dead] Rebirth; [@target,dead] Rebirth
/script SendChatMessage("Rezzing "..UnitName("target"), "RAID")
```
> [!tip] Why it's valuable
> Combat rezzes are a **raid-limited resource** — using them wisely matters. This macro rezzes the dead player you hover (or target) and announces it so the raid knows. **Why valuable:** a dead DPS is lost raid DPS; a dead tank is a wipe. One key from raid frames = instant recovery. *(The announce keeps officers informed so the next rez is assigned properly.)*

### Nature's Swiftness + Healing Touch (instant big heal)
```lua
#showtooltip
/cast Nature's Swiftness
/cast Healing Touch
```


> [!tip] Why it's valuable
> Nature's Swiftness makes the next heal instant + free — this is the druid's 'tank is at 10%, heal NOW' button. Two abilities, one GCD.

### Nature's Swiftness + Regrowth (instant save)
```lua
#showtooltip
/cast Nature's Swiftness
/cast [@mouseover,help,nodead][@player] Regrowth
```
> [!tip] Why it's valuable
> Nature's Swiftness makes the next heal **instant + free**. Pairing it with Regrowth (direct + HoT) gives you a big instant heal with a HoT attached — the resto raid "save the tank NOW" macro. **Why valuable:** a single instant big-heal beats a 3.5s cast when the tank is at 10%.

### Gift of the Wild (raid-wide buff)
```lua
#showtooltip
/cast Gift of the Wild
```
> [!tip] Why it's valuable
> **Gift of the Wild** is the classic druid raid buff — all stats, all resists, and armor on every party member in one cast. **Why valuable:** it's your cast-every-30-minutes raid duty; a dedicated key makes re-buffing after a wipe one press instead of twenty.

### Abolish Poison (self/mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Abolish Poison
```


> [!tip] Why it's valuable
> Removes AND prevents poison for a duration — the anti-poison-boss tool. Mouseover-first so you can cleanse the tank without dropping your own healing target.

### Dispel Combo (Remove Curse + Abolish Poison)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Remove Curse
/cast [@mouseover,help,nodead][@player] Abolish Poison
```
> [!tip] Why it's valuable
> Both druid dispels on one key — curse OR poison, whoever you hover. **Why valuable:** raid fights mix debuff types; one button covers both without you checking what's on the target. Mouseover-first = dispel the tank in raid frames without losing your target.

---

## 🐾 Feral DPS (Cat Form)

### Prowl (stealth)
```lua
#showtooltip
/cast [nostealth] Prowl
```


> [!tip] Why it's valuable
> Cat-form stealth — the druid's opener and escape tool. Nostealth guard prevents wasted presses while already hidden.

### Ravage Opener (stealth-only)
```lua
#showtooltip
/cast [stealth] Ravage; [nostealth] Claw
```
*(In stealth → Ravage. Out of stealth → Claw. Perfect single-button opener — no Mangle on Forever.)*


> [!tip] Why it's valuable
> Ravage from stealth is the feral's biggest opening hit; out of stealth the same key falls back to Claw. One button, always the right opener — no Mangle on Forever.

### Feral Raid Opener (prowl + ravage + FF)
```lua
#showtooltip
/cast [nostealth] Prowl
/cast [stealth] Ravage
/cast [stealth] Faerie Fire
```
> [!tip] Why it's valuable
> Boss pulls start with you out of cat or in travel form. One key: enter stealth → Ravage from stealth (bonus damage) → Faerie Fire (armor shred) before the tank even finishes the pull. **Why valuable:** Ravage-from-stealth is your biggest opening hit, and the FF debuff helps the whole raid's physical DPS from second zero.

### Claw (cat CP builder — form-guard)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Claw
/startattack
```
> [!tip] Why it's valuable
> Claw is the classic cat's basic **combo-point builder** — the fallback when Rake's bleed is already up or Shred can't be used (target facing you). The form guard means you're never stuck in caster form pressing it. **Why valuable:** a cat that's not building CPs is a cat doing zero damage; this button keeps you in form and attacking from any state.

### Rake (cat bleed + CP builder)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Rake
/startattack
```
> [!warning] Mangle removed
> Mangle (TBC+) doesn't exist on Forever. Rake (level 24) is the classic cat's bleed + combo-point builder — refresh the bleed every ~8s, use Shred between refreshes. **Why valuable:** bleeds scale with your gear, so Rake uptime is a hidden DPS meter.

### Shred (behind target — form-guard)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Shred
/startattack
```
> [!tip] Why it's valuable
> **Shred is the classic cat's hardest-hitting CP builder** — big damage from behind the target, feeding Rip and Ferocious Bite. The form guard means you're never stuck in caster form pressing it. **Why valuable:** with no Mangle or Tiger's Fury on a Classic-era server, crits and CP generation are your whole damage profile — Shred behind the boss is the core of raid cat DPS.

### Full Cat Burst (Berserk + trinket)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Berserk
/use 13
```
> [!tip] Why it's valuable
> The feral raid burst window: **Berserk (talent)** — 50% energy costs for 15s — plus your trinket proc, stacked into the boss's damage window. **Why overlapping matters:** during Berserk you can chain Shred/Rip non-stop; the trinket on the same key makes every global in that window hit harder. One key = the whole burn phase. *(Tiger's Fury is TBC+ and doesn't exist on Forever.)*

### Berserk (talent burst)
```lua
#showtooltip
/cast Berserk
```
> [!warning] Tiger's Fury removed
> Tiger's Fury (TBC+) doesn't exist on Forever. Berserk (talent) is the classic-era cat burst — 50% energy costs for 15s, so you can chain Shred/Rip without waiting on energy.

### Rip (5-CP DoT finisher)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Rip
```
> [!tip] Why it's valuable
> Rip is the feral's strongest single-target damage (a 5-CP bleed). A dedicated key with a clear icon makes the "refresh before it falls" timing obvious. **Why valuable:** Rip's tick damage outpaces Ferocious Bite at full CPs on long fights — knowing which finisher to press is what separates good ferals from great ones. *(Bind Rip and Ferocious Bite next to each other; refresh Rip, dump excess CPs into FB.)*

### Ferocious Bite (direct finisher)
```lua
#showtooltip
/cast Ferocious Bite
```


> [!tip] Why it's valuable
> The cat's damage finisher — dumps combo points for a big hit (scales with AP). The 'spend the CPs' button for targets that won't live through Rip.

### Primal Bite (talent finisher)
```lua
#showtooltip
/cast Primal Bite
```
*(Talent finisher — add to the bar once you've specced into it.)*


> [!tip] Why it's valuable
> The classic feral finisher talent — a burst alternative to Rip/Ferocious Bite. Add to the bar once specced; greys out before that.

### Dash (speed burst)
```lua
#showtooltip
/cast Dash
```


> [!tip] Why it's valuable
> Cat-form speed burst — the chase-and-escape key. Cat-only, so bind it near your Cat Form button.

### Pounce (stealth stun — level 36)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast [stealth] Pounce
```
> [!warning] Survival Instincts removed
> Survival Instincts (TBC+) doesn't exist on Forever. Pounce (36) is the classic cat's opening stun — good for add control and PvP openers. *(Maim is WotLK+ and doesn't exist on Forever.)*

### Cower (threat dump)
```lua
#showtooltip
/cast Cower
```


> [!tip] Why it's valuable
> Reduces your threat in cat form — the 'stop pulling off the tank' button when your bleeds are generating too much aggro.

---

## 🐻 Feral Tank (Bear Form)

### Bear Form + Enrage (rage engine)
```lua
#showtooltip
/cast [nostance:1] Bear Form
/cast Enrage
```


> [!tip] Why it's valuable
> Enrage fills your rage bar on entering bear — the correct tank opener that makes your first few Mauls/Lacerates free. One key for the whole ramp.

### Lacerate Stacker (bear bleed + threat)
```lua
#showtooltip
/cast [nostance:1] Bear Form
/castsequence reset=target Lacerate, Lacerate, Lacerate, Lacerate, Lacerate
```
> [!tip] Why it's valuable
> Lacerate (level 42) is the classic bear's **bleed-stack + threat generator** — up to 5 stacks, each doing damage and generating threat. This button cycles through the stacks and auto-resets when you switch targets. **Why valuable:** a stacked Lacerate is your main raid threat source AND a passive DPS bleed — this macro keeps all 5 stacks up without you counting them mid-fight.

### Bear Pull (Enrage + Lacerate opener)
```lua
#showtooltip
/cast [nostance:1] Bear Form
/cast Enrage
/cast Lacerate
/startattack
```
> [!tip] Why it's valuable
> The correct bear pull: Enrage fills your rage bar (more threat, faster), Lacerate starts the bleed stack, auto-attack engaged. **Why valuable:** opening with Enrage means your first Lacerates cost nothing and your threat lead is huge — DPS can burst from second one instead of waiting for you to build aggro.

### Swipe (AoE threat)
```lua
#showtooltip
/cast Swipe
```


> [!tip] Why it's valuable
> Bear AoE threat generator — the 'grab the pack' button for multi-target pulls. Every add that isn't swiped is an add heading for your healer.

### Maul (single-target threat — form-guard)
```lua
#showtooltip
/cast [nostance:1] Bear Form
/cast Maul
/startattack
```
> [!tip] Why it's valuable
> **Maul is the bear's single-target threat spike** — it converts rage into an on-next-swing attack with bonus threat, and it feeds your Lacerate stack. One button: shift to bear, Maul, engage. **Why valuable:** on single-target bosses Maul-on-cooldown is the bear's threat core; binding it with the form shift means you're never caught in caster form during a tank swap. *(Mangle is TBC+ and doesn't exist on Forever.)*

### Demoralizing Roar (AoE attack debuff)
```lua
#showtooltip
/cast Demoralizing Roar
```


> [!tip] Why it's valuable
> Reduces all nearby enemies' attack power — the bear's group-wide mitigation. Press on pull so the pack hits softer for the whole fight.

### Growl (taunt)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][@focus,harm,nodead][] Growl
```


> [!tip] Why it's valuable
> Bear taunt with mouseover→focus→target priority — the 'get it off the healer NOW' key. Priority chain means no target-switching during an emergency.

### Bash (stun)
```lua
#showtooltip
/cast Bash
```


> [!tip] Why it's valuable
> 5-second stun in bear form — the tank's interrupt/CC for caster adds and boss mechanics. One key, no form check needed.

### Frenzied Regeneration (self-heal)
```lua
#showtooltip
/cast [@player] Frenzied Regeneration
```


> [!tip] Why it's valuable
> Converts rage into health over 10s — the bear's self-heal. Self-cast guard means it always lands on you even if a friendly is targeted.

### Bear Panic (Barkskin + Frenzied Regeneration)
```lua
#showtooltip
/cast Barkskin
/cast [@player] Frenzied Regeneration
```
> [!tip] Why it's valuable
> The bear's **oh-crap button**: Barkskin (20% damage reduction) + Frenzied Regeneration (convert rage to health over 10s) — two defensives in one press. **Why valuable:** raid bosses hit hard; a tank has ~2 seconds to react to a bad debuff stack. One key beats two panicked keypresses. *(Survival Instincts is TBC+ and doesn't exist on Forever. Drop your defensive potion in line 3 if you want a third layer.)*

### Feral Charge (gap closer)
```lua
#showtooltip
/cast Feral Charge
```


> [!tip] Why it's valuable
> Bear/cat charge to the target — the druid's gap-closer and stun-interrupt. Talent-gated in Feral Combat.

### Challenging Roar (AoE taunt)
```lua
#showtooltip
/cast Challenging Roar
```


> [!tip] Why it's valuable
> Taunts everything in range — the 'oh crap, adds everywhere' button. Long cooldown, but it's the bear's raid-saving taunt.

### Faerie Fire (Feral) — raid debuff duty
```lua
#showtooltip
/cast [@focus,harm,nodead] Faerie Fire; [@mouseover,harm,nodead] Faerie Fire
```
> [!tip] Why it's valuable
> Faerie Fire (-armor) is a **raid-wide physical DPS multiplier** — bosses need it up 100%. This macro keeps it on your focus (the boss) without breaking your target. **Why valuable:** druids are often the only FF source in a raid; a missing FF is 5% physical DPS loss for everyone. One key, always applied.

---

## 🔮 Balance (Moonkin)

### Wrath (fast nuke — form-guard)
```lua
#showtooltip
/cast [nostance:5] Moonkin Form
/cast Wrath
```
> [!tip] Why it's valuable
> Wrath is your filler; being stuck out of moonkin form (resurrection, dispel, shapeshift hiccup) while spamming it wastes the moonkin crit buff. **Why valuable:** the form guard line means every Wrath press also guarantees the form — one key, always optimal.

### Starfire (big nuke)
```lua
#showtooltip
/cast Starfire
```


> [!tip] Why it's valuable
> The balance druid's big slow nuke — hardest single hit in the kit. Pairs with Moonfire DoT and Insect Swarm for the full rotation.

### Moonfire (instant DoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Moonfire
```


> [!tip] Why it's valuable
> Instant, no-mana-after-first-cost DoT that also opens fights — the balance 'always up' debuff. Mouseover lets you tag adds or PvP targets instantly.

### Insect Swarm (talent DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Insect Swarm
```


> [!tip] Why it's valuable
> DoT that reduces the target's hit chance — balance damage + mitigation in one. Talent-gated until you spend Balance points.

### Moonfire + Insect Swarm Dual-Dot
```lua
#showtooltip
/castsequence reset=8 Moonfire, Insect Swarm, Moonfire, Insect Swarm
```
> [!tip] Why it's valuable
> Both balance DoTs on one button, kept fresh on the current target. **Why valuable:** DoT uptime is the balance druid's whole damage profile — a dropped Moonfire or Swarm is lost DPS every tick it's missing. This button manages both refresh timers for you, freeing your attention for movement mechanics.

### Faerie Fire (armor debuff)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Faerie Fire
```


> [!tip] Why it's valuable
> Reduces target armor — the raid-wide physical DPS multiplier. If you're the only druid, this 100% uptime is your most important debuff.

### Hurricane (AoE channel — form-guard)
```lua
#showtooltip
/cast [nostance:5] Moonkin Form
/cast Hurricane
```
> [!tip] Why it's valuable
> **Hurricane is the classic balance druid's AoE** — a channelled windstorm that damages everything in a wide area for 10s. **Why valuable:** on AoE-heavy trash and packs it's the druid's only real AoE damage; the Moonkin guard keeps the 10% crit aura up while you channel. *(Starfall is WotLK+ and doesn't exist on Forever.)*

### Balance Survival (Nature's Grasp + Barkskin)
```lua
#showtooltip
/cast Nature's Grasp
/cast Barkskin
```
> [!tip] Why it's valuable
> With no Starfall or Force of Nature on Forever, the balance raid survival kit is your burst: **Nature's Grasp** roots any attacker (procs per hit for 45s) while **Barkskin** cuts incoming damage. **Why valuable:** casters who survive the add-swarm keep DPSing — this is the one-key "don't die to the pack" button. *(Force of Nature is TBC+ and doesn't exist on Forever.)*

### Nature's Grasp (root attackers on hit)
```lua
#showtooltip
/cast Nature's Grasp
```
> [!warning] Force of Nature removed
> Force of Nature (TBC+) doesn't exist on Forever. Nature's Grasp is the classic balance survival tool — 45s buff that roots anything that melees you.

### Barkskin (damage reduction)
```lua
#showtooltip
/cast Barkskin
```


> [!tip] Why it's valuable
> Instant 20% damage reduction — the druid's 'I'm being focused' button. Works in any form; the universal panic mitigation.

### Moonfire + Wrath rotation (single button)
```lua
#showtooltip
/castsequence reset=6 Moonfire, Wrath, Wrath, Wrath
```


> [!tip] Why it's valuable
> One key runs the classic balance rotation: Moonfire, then Wrath x3, then reset — DoT uptime with zero timer-watching. The 'lazy but optimal' DPS key.

---

## 🧊 Utility & Control

### Omen of Clarity (free spell proc — mouseover)
```lua
#showtooltip
/cast Omen of Clarity
```
> [!warning] Cyclone removed
> Cyclone (TBC+) doesn't exist on Forever — classic CC is Hibernate and Entangling Roots below. Omen of Clarity is the classic proccy buff: your next damage/heal spell costs no mana.

### Entangling Roots (root)
```lua
#showtooltip
/cast Entangling Roots
```


> [!tip] Why it's valuable
> Roots a target in place — the druid's kiting and CC tool. Keeps melee off you or locks an add while the tank picks it up.

### Mark of the Wild (party buff)
```lua
#showtooltip
/cast Mark of the Wild
```


> [!tip] Why it's valuable
> The druid's party buff — stats, armor, all resists in one cast. The 'buff the party after every wipe' key.

### Thorns (self/mouseover buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Thorns
```


> [!tip] Why it's valuable
> Reflects melee damage — free DPS on anything that hits the tank (or you). Mouseover-first so you can thorns the MT in raids.

### Remove Curse (self/mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Remove Curse
```


> [!tip] Why it's valuable
> The druid's curse dispel — mouseover-first so you cleanse raid frames without losing your heal target. A curse left on the tank is a dead tank.

### Hibernate (beast/serpent CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead] Hibernate; [@mouseover,harm,nodead] Hibernate
```
> [!tip] Why it's valuable
> Hibernate is the druid's **raid CC for beast/dragonkin adds** — 40 seconds of CC (or until damaged). Focus-based means you control the assigned add without retargeting. **Why valuable:** on trash/add phases, a hibernated add is a non-factor; the tank can pull packs safely knowing the dangerous beast is asleep.

### Soothe Animal (remove enrage)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Soothe Animal
```
*(Forever renames Soothe → Soothe Animal.)*
> [!tip] Why it's valuable
> Removes enrage effects from beasts — the classic "calm the raging mob" utility. Focus-based so you can calm the dangerous add without retargeting.

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Rake / Wrath | Main build/nuke |
| 2 | Ravage Opener | Stealth opener |
| 3 | Rip / Ferocious Bite | Finisher |
| 4 | Berserk (talent) | Burst |
| Q | Growl / Faerie Fire | Debuff |
| E | Dash / Feral Charge | Mobility |
| R | Rejuvenation | Mouseover HoT |
| F | Healing Touch | Mouseover heal |
| Shift-F | Dispel Combo | Curse+poison one key |
| G | Bear Panic | Barkskin + Frenzied Regen |
| Shift-1 | Shift-to-heal-and-back | Leveling heal |
| Mouse4 | Travel Form / Travel+Stealth | Travel |

---

> [!note] Custom server check
> WoW: Forever is a **Classic-era (level 60) client** — no Mangle, Tiger's Fury, Survival Instincts, Cyclone, Flight Form, Force of Nature, Lifebloom, Tree of Life, Starfall, Savage Roar, or Maim. The macros above use the classic kit: Claw/Rake/Shred for cat CPs, Rip/Ferocious Bite/Primal Bite (talent) finishers, Pounce (36) stun, Lacerate (42) stacker + Dire Bear Form (40) for bear, Hurricane for balance AoE, Soothe Animal, and Revive/Rebirth for rez. Form stances are fixed: Bear=1, Aquatic=2, Cat=3, Travel=4, Moonkin=5. If a spell is greyed out it's talent-gated (Swiftmend, Wild Growth, Insect Swarm, Berserk, Feral Charge, Primal Bite, Moonkin Form) — spend the points and the same macro works.