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

### Multi-Shot (AoE)
```lua
#showtooltip
/cast Multi-Shot
```

### Serpent Sting (DoT)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Serpent Sting
```

### Hunter's Mark
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Hunter's Mark
```

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

### Concussive Shot (interrupt / stun)
```lua
#showtooltip
/cast Concussive Shot
```

---

## 🐾 Pet Control

### Bestial Wrath + Pet Attack (talent burst)
```lua
#showtooltip
/petattack
/cast Bestial Wrath
```

### Pet Follow (break combat)
```lua
/petfollow
```

### Pet Passive (stop attacking)
```lua
/petpassive
```

### Mend Pet (mouseover or self-pet)
```lua
#showtooltip
/cast [@pet] Mend Pet
```

### Revive Pet (instant)
```lua
#showtooltip
/cast Revive Pet
```

### Call Pet + Dismiss toggle
```lua
#showtooltip
/cast Call Pet
```

### Feed Pet (quick)
```lua
#showtooltip
/cast Feed Pet
/use [nomod] Roasted Quail
```

### Pet Buff Check
```lua
#showtooltip
/run local n=UnitName("pet"); if n then print(n.." — "..GetPetHappiness()) end
```

---

## 🪤 Traps & Crowd Control

### Freezing Trap (targeted ground)
```lua
#showtooltip
/cast Freezing Trap
```

### Explosive Trap
```lua
#showtooltip
/cast Explosive Trap
```

### Frost Trap (slow)
```lua
#showtooltip
/cast Frost Trap
```

### Feign Death (drop aggro)
```lua
#showtooltip
/cast Feign Death
```

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

### Rapid Fire (haste burst)
```lua
#showtooltip
/cast Rapid Fire
```

### Bestial Wrath (pet burst + immunity)
```lua
#showtooltip
/cast Bestial Wrath
/petattack
```

### Eagle Eye (scouting)
```lua
#showtooltip
/cast Eagle Eye
```

### Deterrence (dodge everything)
```lua
#showtooltip
/cast Deterrence
```

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