# Priest Macros — WoW: Forever

Mouseover healing, dispels, and shadow DPS. Classic-era (1.60.1) Priest — works for Holy/Disc/Shadow specs.

> [!tip] Healing macros
> Every heal below is **mouseover-first** (heals whoever you hover) with **self-cast fallback** when no mouseover. Hover the raid frame, press, done.

---

## 💚 Healing (Holy/Disc)

### Flash Heal (fast mouseover heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Flash Heal
```

> [!tip] Why it's valuable
> Mouseover-first with a self-cast fallback - hover the raid frame and press, no target switching; the fastest reactive heal in your kit.

### Renew (HoT mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Renew
```

> [!tip] Why it's valuable
> The same mouseover pattern lets you blanket HoTs across the raid without ever changing target - one press per player, no healing downtime.

### Greater Heal (big slow heal)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Greater Heal
```

> [!tip] Why it's valuable
> One key for your big heal, aimed by mouseover or self - reaction-time friendly when the tank spikes and you need maximum throughput immediately.

### Prayer of Healing (party AoE)
```lua
#showtooltip
/cast Prayer of Healing
```

> [!tip] Why it's valuable
> Party-wide heal on a single keybind - the emergency button that tops up the whole group at once instead of five separate casts.

### Power Word: Shield (mouseover bubble)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Power Word: Shield
```

> [!tip] Why it's valuable
> Mouseover bubble with self-fallback - pre-emptive absorbs land a full GCD earlier than target-then-cast, which is exactly when shields save lives.

### Binding Heal (self + target — talent)
```lua
#showtooltip
/cast [@mouseover,help,nodead] Binding Heal
```
*(Talent-gated (Holy tree). Classic's version of the instant "heal me + heal target" button.)*

> [!tip] Why it's valuable
> One press heals both you and your mouseover target - the self+target efficiency that keeps you alive while you save someone else.

### Desperate Prayer (self emergency)
```lua
#showtooltip
/cast [@player] Desperate Prayer
```
> [!warning] Classic save
> Desperate Prayer + Power Word: Shield is your classic big-save combo — no Guardian Spirit in 1.60.1.

---

## 🧹 Dispels & Cures

### Dispel Magic (mouseover, both directions)
```lua
#showtooltip
/cast [@mouseover,harm,nodead] Dispel Magic; [@mouseover,help,nodead] Dispel Magic; [harm] Dispel Magic; [help] Dispel Magic
```

> [!tip] Why it's valuable
> The four-condition chain purges enemies AND cures allies from the same key - mouseover or target, harm or help, one button does it all.

### Cure Disease (mouseover)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Cure Disease
```

> [!tip] Why it's valuable
> Mouseover cure with self-fallback - diseases get removed a full reaction faster, and you never accidentally cure the wrong person.

### Abolish Disease (self)
```lua
#showtooltip
/cast [@player] Abolish Disease
```
*(Classic has no Mass Dispel — single-target Dispel Magic is your only purge. No AoE dispel exists in 1.60.1.)*

> [!tip] Why it's valuable
> A dedicated self-cleanse key - one press strips diseases off you repeatedly, so you stay debuff-free without hunting for the button mid-fight.

---

## 🌑 Shadow DPS

### Shadow Word: Pain (DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Shadow Word: Pain
```

> [!tip] Why it's valuable
> Mouseover DoT application - dot up adds without ever dropping your main target, keeping your rotation and focus intact.

### Mind Blast (nuke)
```lua
#showtooltip
/cast Mind Blast
/startattack
```

> [!tip] Why it's valuable
> Nuke plus /startattack in one press - instant damage that also keeps your auto-attacks rolling, the backbone of the shadow rotation.

### Mind Flay (channel — talent)
```lua
#showtooltip
/cast Mind Flay
```

> [!tip] Why it's valuable
> One key starts your channel immediately - no delay between GCDs, and the instant cast lets you react to procs or movement windows faster.

### Devouring Plague (DoT + heal)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Devouring Plague
```

> [!tip] Why it's valuable
> Mouseover DoT that also heals you - damage and self-sustain from a single button, ideal for solo play or while kiting.

### Holy Nova (AoE — talent)
```lua
#showtooltip
/cast Holy Nova
```
*(Talent-gated (Holy tree). The classic instant AoE that damages enemies **and** heals the party — replaces Mind Sear for AoE.)*

> [!tip] Why it's valuable
> One key instant AoE that damages enemies and heals the party - your only multi-target option in Classic, saving a full cast when adds or raid damage spike.

### Shadowform (toggle — talent)
```lua
#showtooltip
/cast Shadowform
```

> [!tip] Why it's valuable
> A dedicated toggle key for Shadowform - one press flips your damage mode on and off, no spellbook fumbling between pulls.

### Vampiric Embrace (self-heal on damage — talent)
```lua
#showtooltip
/cast Vampiric Embrace
```

> [!tip] Why it's valuable
> One press converts your shadow damage into healing - self-sustain that keeps you casting through fights instead of stopping to heal.

### Silence (interrupt — focus, talent)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Silence
```

> [!tip] Why it's valuable
> Focus-first interrupt - lock down a caster without switching targets, the reaction-time tool for deadly enemy spells.

---

## 🧊 Utility & Buffs

### Power Word: Fortitude (party buff)
```lua
#showtooltip
/cast Power Word: Fortitude
```

> [!tip] Why it's valuable
> One press buffs the whole party's stamina - the pre-pull routine that takes a single keybind instead of five individual casts.

### Divine Spirit (spirit buff)
```lua
#showtooltip
/cast Divine Spirit
```

> [!tip] Why it's valuable
> Party spirit buff on one key - more mana regen and spell power for everyone, applied between pulls in a single press.

### Inner Fire (armor buff)
```lua
#showtooltip
/cast Inner Fire
```

> [!tip] Why it's valuable
> One key keeps your armor buff up - a simple pre-pull press that noticeably reduces physical damage taken all fight.

### Fear Ward (pre-fight buff)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Fear Ward
```

> [!tip] Why it's valuable
> Mouseover or self-cast fear immunity on one key - the classic pre-fight buff that makes fear-heavy bosses trivial.

### Psychic Scream (fear)
```lua
#showtooltip
/cast Psychic Scream
```

> [!tip] Why it's valuable
> Instant AoE fear on a single key - the panic button that buys seconds when enemies close in, no targeting required.

### Shackle Undead (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Shackle Undead
```

> [!tip] Why it's valuable
> Focus-first CC locks down a second undead without retargeting - the key that makes undead pulls like Scholomance packs manageable.

### Power Infusion (haste burst — self/target, talent)
```lua
#showtooltip
/cast [@mouseover,help,nodead][@player] Power Infusion
```

> [!tip] Why it's valuable
> Mouseover haste buff with self-fallback - one press spikes your own or a DPS's cast speed at the right moment without retargeting.

### Mana Burn (burn enemy mana)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Mana Burn
```

> [!tip] Why it's valuable
> Mouseover burn targets enemy mana - the PvP and caster-killing tool that punishes healers from range on a single key.

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Flash Heal | Fast heal |
| 2 | Renew | HoT |
| 3 | Greater Heal | Big heal |
| 4 | Power Word: Shield | Bubble |
| Q | Dispel Magic | Purge |
| E | Psychic Scream | Fear |
| R | Prayer of Healing | Party save |
| F | Desperate Prayer | Emergency |
| Shift-1 | Power Infusion | Burst |
| Mouse4 | Renew | Mouseover HoT |

---

> [!note] Custom server check
> Verify against your Spellbook on Forever: **Penance** and **Prayer of Mending** exist as Forever talents — if you've skilled them, add mouseover macros with the same `[@mouseover,help,nodead]` pattern. Holy Nova is talent-gated, so it only works with 1+ point in it. There is no Circle of Healing / Guardian Spirit / Lightwell / Mass Dispel in 1.60.1 — don't trust addon suggestions that list them.
