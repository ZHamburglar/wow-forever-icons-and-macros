# Hunter Macros — WoW: Forever

Aspect juggling, pet micro, trap tricks, and the classic Feign Death + Trap combo. Classic-era (Forever) Hunter.

> [!tip] Pet macros
> Pet spells are controlled with `/petattack`, `/petfollow`, `/petpassive` — no targeting needed.

---

## 🎯 Rotation & Damage

> [!note] Classic shots
> Steady Shot, Explosive Shot, and Chimera Shot are not available in Classic (Forever). Use **Arcane Shot** and **Aimed Shot** as your core instant/filler shots.

### Arcane Shot + Auto Shot
```lua
#showtooltip
/cast !Auto Shot
/cast Arcane Shot
```

> [!tip] Why it's valuable
> One button weaves Auto Shot between Arcane Shot casts - no manual auto-attack babysitting, so damage keeps flowing while you focus on positioning.

### Multi-Shot (AoE)
```lua
#showtooltip
/cast Multi-Shot
```

> [!tip] Why it's valuable
> A single keybind for your only Classic AoE shot - instantly hits every enemy in front of you, ideal for pulling packs or multi-target fights.

### Serpent Sting (DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Serpent Sting
```

> [!tip] Why it's valuable
> The mouseover-first targeting applies the DoT to whoever you hover without switching targets - ticking damage stays up while your focus stays on the main kill.

### Hunter's Mark
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Hunter's Mark
```

> [!tip] Why it's valuable
> Mouseover casting applies the mark without breaking your target - your pet and shots immediately get the bonus attack power, so the mark never gets forgotten mid-fight.

### Bestial Wrath (talent — pet burst)
```lua
#showtooltip
/cast Bestial Wrath
/petattack
```
> [!tip] Bestial Wrath replaces Kill Command
> Kill Command is not available in Classic. **Bestial Wrath** (tier 6 Beast Mastery talent) is the pet burst equivalent — add `/petattack` after to send your pet in immediately.

### Aimed Shot (ranged heavy hit)
```lua
#showtooltip
/cast Aimed Shot
```

> [!tip] Why it's valuable
> Your hardest-hitting ranged shot on one key - a dedicated burst button for when raw damage matters more than cast speed.

### Concussive Shot (interrupt / stun)
```lua
#showtooltip
/cast Concussive Shot
```

> [!tip] Why it's valuable
> A ranged stun on a single keybind lets you stop a runner or interrupt a cast from distance - a reaction-time save when melee cannot reach.

---

## 🐾 Pet Control

### Bestial Wrath + Pet Attack (talent burst)
```lua
#showtooltip
/petattack
/cast Bestial Wrath
```

> [!tip] Why it's valuable
> One press sends the pet in AND pops the burst - no fumbling for two keys mid-combat, and the pet lands its first hit instantly.

### Pet Follow (break combat)
```lua
/petfollow
```

> [!tip] Why it's valuable
> A dedicated key breaks your pet out of combat and brings it back - saves the pet (and your Mend Pet casts) when it over-aggros or chases a fleeing add.

### Pet Passive (stop attacking)
```lua
/petpassive
```

> [!tip] Why it's valuable
> Instantly stops your pet's attacks without retargeting - the fastest way to drop pet aggro or halt an unwanted pull.

### Mend Pet (mouseover or self-pet)
```lua
#showtooltip
/cast [@pet] Mend Pet
```

> [!tip] Why it's valuable
> Casts directly on your pet with no targeting step - one press mid-fight keeps your pet alive with zero risk of healing the wrong unit.

### Revive Pet (instant)
```lua
#showtooltip
/cast Revive Pet
```

> [!tip] Why it's valuable
> One key brings your pet back the moment it dies - no spellbook digging or targeting, so downtime between pet deaths is minimal.

### Call Pet + Dismiss toggle
```lua
#showtooltip
/cast Call Pet
```

> [!tip] Why it's valuable
> Summons your pet with one keypress and no targeting needed - the same button works as the toggle point for dismissing later.

### Feed Pet (quick)
```lua
#showtooltip
/cast Feed Pet
/use [nomod] Roasted Quail
```

> [!tip] Why it's valuable
> Casts Feed Pet and eats Roasted Quail in one press - keeps happiness topped up between fights without dragging food onto your bars.

### Pet Buff Check
```lua
#showtooltip
/run local n=UnitName("pet"); if n then print(n.." — "..GetPetHappiness()) end
```

> [!tip] Why it's valuable
> Prints your pet's name and happiness on demand - a fast sanity check that your pet is the right one and loyal enough to keep fighting.

---

## 🪤 Traps & Crowd Control

### Freezing Trap (targeted ground)
```lua
#showtooltip
/cast Freezing Trap
```

> [!tip] Why it's valuable
> One key lays the trap at your feet for instant crowd control - a reaction-time save on incoming adds with no trap-type cycling.

### Explosive Trap
```lua
#showtooltip
/cast Explosive Trap
```

> [!tip] Why it's valuable
> AoE fire damage on a single key - drop it under a pack for free cleave, and the flames keep burning anything that walks over them.

### Frost Trap (slow)
```lua
#showtooltip
/cast Frost Trap
```

> [!tip] Why it's valuable
> A ground AoE slow that holds multiple enemies at range - one press makes kiting dramatically safer.

### Feign Death (drop aggro)
```lua
#showtooltip
/cast Feign Death
```

> [!tip] Why it's valuable
> Drops all aggro instantly on one keybind - the classic panic button and the setup for every safe re-trap or out-of-combat drink.

### Feign Death + Freezing Trap (instant re-trap)
```lua
#showtooltip
/castsequence reset=5 Feign Death, Freezing Trap
```
> [!tip] FD+Trap
> The classic "FD trap" for pulling — Feign Death drops aggro, then the trap lands. Sequence resets after 5s idle.

---

## 🧊 Utility & Mobility

### Disengage (backflip)
```lua
#showtooltip
/cast Disengage
```

> [!tip] Why it's valuable
> One key flips you backward out of melee - instantly creates the range your shots need or escapes a sticky situation.

### Aspect of the Hawk (ranged AP buff)
```lua
#showtooltip
/cast Aspect of the Hawk
```
> [!warning] Mana regen
> Classic hunters switch between **Aspect of the Hawk** (AP) and **Aspect of the Monkey** (mana regen). Aspect of the Viper does not exist in Classic.

### Aspect of the Cheetah (travel)
```lua
#showtooltip
/cast Aspect of the Cheetah
```

> [!tip] Why it's valuable
> A single keybind for travel speed - swap in for movement-heavy sections and escape or catch up without hunting the spellbook.

### Rapid Fire (haste burst)
```lua
#showtooltip
/cast Rapid Fire
```

> [!tip] Why it's valuable
> Haste burst on one key - stack it with your shots for a spike window and line it up with trinkets without losing a GCD.

### Bestial Wrath (pet burst + immunity)
```lua
#showtooltip
/cast Bestial Wrath
/petattack
```

> [!tip] Why it's valuable
> One press gives your pet burst damage AND damage immunity while sending it in - a huge survivability swing for the pet in tight fights.

### Eagle Eye (scouting)
```lua
#showtooltip
/cast Eagle Eye
```

> [!tip] Why it's valuable
> Scout from range on a single key - the classic pre-pull reconnaissance tool that lets you pull with knowledge instead of surprises.

### Deterrence (dodge everything)
```lua
#showtooltip
/cast Deterrence
```

> [!tip] Why it's valuable
> A dedicated defensive key that dodges melee attacks - a reaction-time save when something reaches you and Disengage is on cooldown.

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|-----|-------|-----|
| 1 | Aimed Shot | Heavy hit |
| 2 | Arcane Shot | Instant |
| 3 | Serpent Sting | DoT |
| 4 | Multi-Shot | AoE |
| Q | Freezing Trap | CC |
| E | Bestial Wrath | Pet burst |
| R | Feign Death | Survival |
| F | Disengage | Mobility |
| Shift-1 | Rapid Fire | Burst |
| Mouse4 | Mend Pet | Pet upkeep |

---

> [!note] Custom server check
> Survival vs Marksman depends on your talent spec. If a spell is greyed out (wrong spec), swap the macro's spell for the one your talents give you.
