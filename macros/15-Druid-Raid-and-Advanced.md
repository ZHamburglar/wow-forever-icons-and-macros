# Druid Macro Expansion — Raid & Advanced (WoW: Forever)

The druid kit from file 10 covered the leveling/rotation basics. This file adds the **advanced druid macros** — Classic-era tools for raids: Lacerate stacking, Rake/Shred CP windows, Hurricane AoE, Swiftmend saves, and raid-duty druid macros. Every one has a **"Why it's valuable"** note.

> [!info] Why this file exists
> Druids are the most macro-dependent class in WoW — four forms, three specs, and a healer kit mean more buttons than any other class. These macros compress the *advanced* druid toolkit: raid feral DPS windows, bear tanking threat/bleed stacking, resto raid-saving heals, and balance AoE.

---

# 🐱 Feral DPS (Raid) — New Macros

### Shred (form-guard CP builder)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Shred
/startattack
```
> [!tip] Why it's valuable
> **Shred is the classic cat's hardest-hitting CP builder** — big damage from behind the target, feeding Rip and Ferocious Bite. The form guard means you're never stuck in caster form pressing it. **Why valuable:** with no Mangle or Tiger's Fury on a Classic-era server, crits and CP generation are your whole damage profile — Shred behind the boss is the core of raid cat DPS. *(Savage Roar is WotLK+ and doesn't exist on Forever.)*

### Rake (cat bleed + CP builder)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Rake
/startattack
```
> [!tip] Why it's valuable
> Rake (level 24) is your **bleed AND combo-point builder in one** — refresh the bleed every ~8s, and use Shred for CPs between refreshes. This macro auto-shifts to cat and attacks, so it works from any form. **Why valuable:** bleeds scale with your gear, so Rake uptime is a hidden DPS meter.

### Pounce (stealth stun — level 36)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast [stealth] Pounce
```
> [!tip] Why it's valuable
> The feral **opener stun** for add-control and PvP: Pounce (level 36) stuns for 4s out of stealth and applies a Rake-style bleed. **Why valuable:** it's the classic druid's only hard stun besides Bash — Ravage in, then Pounce locks the add down while your team bursts. *(Maim is WotLK+ and doesn't exist on Forever.)*

### Full Cat Burst (Berserk + trinket)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Berserk
/use 13
```
> [!tip] Why it's valuable
> The feral raid burst window: **Berserk (talent)** — 50% energy costs for 15s — plus your trinket proc, stacked into the boss's damage window. **Why overlapping matters:** during Berserk you can chain Shred/Rip non-stop; the trinket on the same key makes every global in that window hit harder. One key = the whole burn phase. *(Tiger's Fury is TBC+ and doesn't exist on Forever.)*

### Feral Raid Opener (prowl + ravage + FF)
```lua
#showtooltip
/cast [nostealth] Prowl
/cast [stealth] Ravage
/cast [stealth] Faerie Fire
```
> [!tip] Why it's valuable
> Boss pulls start with you out of cat or in travel form. One key: enter stealth → Ravage from stealth (bonus damage) → Faerie Fire (armor shred) before the tank even finishes the pull. **Why valuable:** Ravage-from-stealth is your biggest opening hit, and the FF debuff helps the whole raid's physical DPS from second zero.

### Rip Refresh Tracker (5-CP DoT)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast Rip
```
> [!tip] Why it's valuable
> Rip is the feral's strongest single-target damage (a 5-CP bleed). A dedicated key with a clear icon makes the "refresh before it falls" timing obvious. **Why valuable:** Rip's tick damage outpaces Ferocious Bite at full CPs on long fights — knowing which finisher to press is what separates good ferals from great ones. *(Bind Rip and Ferocious Bite next to each other; refresh Rip, dump excess CPs into FB.)*

---

# 🐻 Feral Tank (Raid) — New Macros

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

### Faerie Fire (Feral) — raid debuff duty
```lua
#showtooltip
/cast [@focus,harm,nodead] Faerie Fire; [@mouseover,harm,nodead] Faerie Fire
```
> [!tip] Why it's valuable
> Faerie Fire (-armor) is a **raid-wide physical DPS multiplier** — bosses need it up 100%. This macro keeps it on your focus (the boss) without breaking your target. **Why valuable:** druids are often the only FF source in a raid; a missing FF is 5% physical DPS loss for everyone. One key, always applied.

### Bear Panic (Barkskin + Frenzied Regeneration)
```lua
#showtooltip
/cast Barkskin
/cast [@player] Frenzied Regeneration
```
> [!tip] Why it's valuable
> The bear's **oh-crap button**: Barkskin (20% damage reduction) + Frenzied Regeneration (convert rage to health over 10s) — two defensives in one press. **Why valuable:** raid bosses hit hard; a tank has ~2 seconds to react to a bad debuff stack. One key beats two panicked keypresses. *(Survival Instincts is TBC+ and doesn't exist on Forever. Drop your defensive potion in line 3 if you want a third layer.)*

### Bear Threat Opener (Maul form-guard)
```lua
#showtooltip
/cast [nostance:1] Bear Form
/cast Maul
/startattack
```
> [!tip] Why it's valuable
> **Maul is the bear's single-target threat spike** — it converts rage into an on-next-swing attack with bonus threat, and it feeds your Lacerate stack. One button: shift to bear, Maul, engage. **Why valuable:** on single-target bosses Maul-on-cooldown is the bear's threat core; binding it with the form shift means you're never caught in caster form during a tank swap. *(Mangle is TBC+ and doesn't exist on Forever.)*

---

# 🌿 Restoration (Raid) — New Macros

### Gift of the Wild (raid-wide buff)
```lua
#showtooltip
/cast Gift of the Wild
```
> [!tip] Why it's valuable
> **Gift of the Wild** is the classic druid raid buff — all stats, all resists, and armor on every party member in one cast. **Why valuable:** it's your cast-every-30-minutes raid duty; a dedicated key makes re-buffing after a wipe one press instead of twenty. *(Lifebloom is TBC+ and doesn't exist on Forever — the resto rotation is Rejuvenation/Regrowth, covered in file 10.)*

### Swiftmend Combo (talent — consume HoT for instant)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Swiftmend
```
> [!tip] Why it's valuable
> Swiftmend consumes a Rejuvenation or Regrowth on the target for an **instant, huge heal** — the resto druid's emergency save. Mouseover-first means you can rescue anyone in the raid frames without changing your main healing target. **Why valuable:** it's instant, it's big, and it's your only true "oh no" button besides Tranquility.

### Rebirth + Announce (combat rez)
```lua
#showtooltip
/cast [@mouseover,dead] Rebirth; [@target,dead] Rebirth
/script SendChatMessage("Rezzing "..UnitName("target"), "RAID")
```
> [!tip] Why it's valuable
> Combat rezzes are a **raid-limited resource** — using them wisely matters. This macro rezzes the dead player you hover (or target) and announces it so the raid knows. **Why valuable:** a dead DPS is lost raid DPS; a dead tank is a wipe. One key from raid frames = instant recovery. *(The announce keeps officers informed so the next rez is assigned properly.)*

### Innervate the Healer (support macro)
```lua
#showtooltip
/cast [@focus,help,nodead] Innervate; [@mouseover,help,nodead] Innervate; [@player] Innervate
```
> [!tip] Why it's valuable
> Innervate restores a **huge chunk of mana over 20s** — on a raid boss that lasts 8 minutes, the difference between "healer out of mana at 60%" and "healer still casting at 100%" is Innervate placement. Set your focus to the mana-hungry healer (priest/shaman), one key gifts them the mana. **Why valuable:** you're not always the best Innervate target — the raid's throughput healer is. This macro makes it one key.

### Tranquility (raid emergency channel)
```lua
#showtooltip
/cast Tranquility
```
> [!tip] Why it's valuable
> **Tranquility is the resto druid's raid-wide emergency heal** — a channeled AoE that heals the whole party every 2s for 10s. **Why valuable:** it's the classic answer to raid-wide damage spikes; on bosses with predictable bursts, pre-casting it turns a wipe into a save. *(Tree of Life is TBC+ and doesn't exist on Forever — classic resto heals from caster form.)*

### Nature's Swiftness + Regrowth (instant save)
```lua
#showtooltip
/cast Nature's Swiftness
/cast [@mouseover,help,nodead][@player] Regrowth
```
> [!tip] Why it's valuable
> Nature's Swiftness makes the next heal **instant + free**. Pairing it with Regrowth (direct + HoT) gives you a big instant heal with a HoT attached — the resto raid "save the tank NOW" macro. **Why valuable:** a single instant big-heal beats a 3.5s cast when the tank is at 10%.

---

# 🔮 Balance (Raid) — New Macros

### Hurricane (raid AoE channel)
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

### Moonfire + Insect Swarm Dual-Dot
```lua
#showtooltip
/castsequence reset=8 Moonfire, Insect Swarm, Moonfire, Insect Swarm
```
> [!tip] Why it's valuable
> Both balance DoTs on one button, kept fresh on the current target. **Why valuable:** DoT uptime is the balance druid's whole damage profile — a dropped Moonfire or Swarm is lost DPS every tick it's missing. This button manages both refresh timers for you, freeing your attention for movement mechanics.

### Wrath Spam with Moonkin Form Guard
```lua
#showtooltip
/cast [nostance:5] Moonkin Form
/cast Wrath
```
> [!tip] Why it's valuable
> Wrath is your filler; being stuck out of moonkin form (resurrection, dispel, shapeshift hiccup) while spamming it wastes the moonkin crit buff. **Why valuable:** the form guard line means every Wrath press also guarantees the form — one key, always optimal.

---

# 🧊 Druid Utility Extras (not in file 10)

### Dispel Combo (Remove Curse + Abolish Poison)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Remove Curse
/cast [@mouseover,help,nodead][@player] Abolish Poison
```
> [!tip] Why it's valuable
> Both druid dispels on one key — curse OR poison, whoever you hover. **Why valuable:** raid fights mix debuff types; one button covers both without you checking what's on the target. Mouseover-first = dispel the tank in raid frames without losing your target.

### Hibernate (beast/dragonkin CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead] Hibernate; [@mouseover,harm,nodead] Hibernate
```
> [!tip] Why it's valuable
> Hibernate is the druid's **raid CC for beast/dragonkin adds** — 40 seconds of CC (or until damaged). Focus-based means you control the assigned add without retargeting. **Why valuable:** on trash/add phases, a hibernated add is a non-factor; the tank can pull packs safely knowing the dangerous beast is asleep.

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

## 📋 Druid Expansion Quick Chart

| Macro | Spec | Why One Key |
|---|---|---|
| Shred (form-guard) | Feral DPS | Hardest CP builder, always in form |
| Rake | Feral DPS | Bleed + CPs in one |
| Pounce | Feral DPS | Stealth stun opener (36) |
| Full Cat Burst | Feral DPS | Berserk+trinket overlap |
| Lacerate stacker | Feral Tank | 5-stack threat + bleed, auto-count |
| Bear pull | Feral Tank | Enrage→Lacerate opener |
| FF focus | Any | Raid-wide armor debuff uptime |
| Bear panic | Feral Tank | Barkskin + Frenzied Regen, 1 press |
| Gift of the Wild | Resto | Raid-wide buff, one cast |
| Swiftmend | Resto | Instant emergency heal |
| Rebirth+announce | Resto | Limited resource, instant rez |
| Innervate healer | Resto | Mana to the right person |
| Tranquility | Resto | Raid emergency channel |
| Hurricane | Balance | Only AoE, form-guarded |
| Dual-dot | Balance | DoT uptime automation |
| Dispel combo | Any | Curse+poison, one key |

---

> [!note] Custom server check
> WoW: Forever is a **Classic-era (level 60) client**. Spells that don't exist here — Savage Roar, Maim, Tiger's Fury, Survival Instincts, Mangle, Force of Nature, Lifebloom, Tree of Life, Starfall — were replaced with classic equivalents (Shred, Rake, Pounce, Berserk, Lacerate, Maul, Hurricane, Nature's Grasp, Gift of the Wild, Tranquility). Talent-gated buttons (Swiftmend, Berserk, Feral Charge, Moonkin Form) grey out until you spend points. If a macro's spell name doesn't match your Spellbook, swap in the exact name — the *pattern* (form-guard, focus-target, castsequence) is what makes these valuable, and it survives any rename.