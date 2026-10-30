# Warlock Macros — WoW: Forever

Life tap, soulstones, pet micro, and the classic Fear/Seduce control. Classic-era Warlock (level 60).

> [!tip] Pet spells
> Warlock pets use `/petattack`, `/petfollow`, `/petpassive` plus pet-specific spells (Seduction for Succubus, Devour Magic for Felhunter). Classic pets: Imp, Voidwalker, Succubus/Incubus, Felhunter — no Felguard.

---

## 💀 Affliction

### Corruption (DoT — mouseover)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Corruption
```

### Curse of the Elements (raid magic-damage curse)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Curse of the Elements
```
> [!warning] Unstable Affliction removed
> Unstable Affliction (TBC+) doesn't exist on Forever. Curse of the Elements is the classic counterpart — it increases the target's spell damage taken and is a raid staple.

### Shadow Bolt (filler)
```lua
#showtooltip
/cast Shadow Bolt
```

### Drain Life (channeled self-heal)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Drain Life
```
> [!warning] Haunt removed
> Haunt (WotLK+) doesn't exist on Forever. Drain Life is the classic Affliction channel that damages the target and heals you.

### Drain Soul (execute + soul shard)
```lua
#showtooltip
/cast Drain Soul
```

### Siphon Life (talent DoT — self-heal)
```lua
#showtooltip
/cast Siphon Life
```
*(Talented in Affliction — greyed out until you spend points.)*

### Bane of Doom (long DoT — doomguard proc)
```lua
#showtooltip
/cast Bane of Doom
```
> [!warning] Seed of Corruption removed
> Seed of Corruption (WotLK+) doesn't exist on Forever. Bane of Doom is the classic long-duration DoT curse — after 1 minute it summons a Doomguard (and a helper!) to fight for you.

### Bane of Agony (DoT curse — mouseover)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Bane of Agony
```
*(Forever renames Curse of Agony → Bane of Agony.)*

---

## 🔥 Destruction

### Incinerate (talent nuke)
```lua
#showtooltip
/cast Incinerate
```
*(Incinerate is a Destruction talent on Forever — take it before keybinding.)*

### Immolate (DoT + Conflagrate fuel)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Immolate
```

### Conflagrate (talent burst after Immolate)
```lua
#showtooltip
/cast Conflagrate
```

### Searing Pain (fast filler)
```lua
#showtooltip
/cast Searing Pain
```
> [!warning] Chaos Bolt removed
> Chaos Bolt (TBC+) doesn't exist on Forever. Searing Pain is the classic instant-cast filler — fast, spammable, and it builds threat, so mind the aggro.

### Shadowburn (talent execute)
```lua
#showtooltip
/cast Shadowburn
```

### Soul Fire (long-cast nuke)
```lua
#showtooltip
/cast Soul Fire
```

### Rain of Fire (AoE)
```lua
#showtooltip
/cast Rain of Fire
```

---

## 🦎 Demonology

### Fel Domination + Instant Summon
```lua
#showtooltip
/cast Fel Domination
/cast [mod:shift] Summon Voidwalker; [mod:ctrl] Summon Succubus; [mod:alt] Summon Felhunter; Summon Imp
```
> [!warning] Metamorphosis removed
> Metamorphosis (TBC+) doesn't exist on Forever. Fel Domination (talent) is the classic summon accelerator — your next pet summon is instant. Press once: buff + summon in one key.

### Demonic Sacrifice (talent — consume pet for buff)
```lua
#showtooltip
/cast Demonic Sacrifice
```
> [!warning] Immolation Aura removed
> Immolation Aura (WotLK+) doesn't exist on Forever. Demonic Sacrifice (talent) is the classic demo cooldown — consume your pet for a 30-minute personal buff (Imp = 15% fire damage, Voidwalker = 3% health/5s, Succubus = 15% shadow damage, Felhunter = 60 all-resist).

### Health Funnel (pet heal)
```lua
#showtooltip
/cast [@pet,nodead] Health Funnel
```
> [!warning] Demonic Empowerment removed
> Demonic Empowerment (WotLK+) doesn't exist on Forever. Health Funnel is the classic pet-heal channel — keep your Voidwalker alive on tanking duty.

### Ritual of Summoning (summon a party member)
```lua
#showtooltip
/cast Ritual of Summoning
```
> [!warning] Summon Felguard removed
> Summon Felguard (TBC+) doesn't exist on Forever — classic pets are Imp, Voidwalker, Succubus/Incubus, Felhunter. Ritual of Summoning is the classic utility that pulls a party member straight to you.

---

## 🐾 Pet Management

### Pet Attack (+ weapon swing)
```lua
#showtooltip
/petattack
/startattack
```
*(Classic pets have no Kill Command; add the pet's situational spell per encounter: Torment, Seduction, Devour Magic, Spell Lock.)*

### Pet Follow
```lua
/petfollow
```

### Pet Passive
```lua
/petpassive
```

### Succubus Seduce (CC)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Seduction
```

### Felhunter Devour Magic (dispels enemy buffs)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Devour Magic
```

### Felhunter Spell Lock (interrupt)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Spell Lock
```

### Voidwalker taunt
```lua
#showtooltip
/cast [@focus,harm,nodead][] Suffering
```

### Pet Summon Quick-Switch
```lua
#showtooltip
/cast [mod:shift] Summon Voidwalker; [mod:ctrl] Summon Succubus; [mod:alt] Summon Felhunter; Summon Imp
```
*(Shift=VW, Ctrl=Succubus, Alt=Felhunter, default=Imp — classic pets only, no Felguard.)*

---

## 🧊 Utility & Control

### Life Tap (mana — with macro warning)
```lua
#showtooltip
/cast Life Tap
```
> [!warning] Life Tap spam
> Life Tap costs HP. Add a health check: `/cast [health>30] Life Tap` — only taps above 30% HP. (Classic has no Dark Pact; Life Tap IS the mana engine.)

### Healthstone (create + use)
```lua
#showtooltip
/cast Create Healthstone
/use Healthstone
```

### Soulstone (create + apply rez buff — mouseover)
```lua
#showtooltip Create Soulstone
/cast Create Soulstone
/use [@mouseover,help,nodead][@player] Soulstone
```
> [!warning] Soulstone renamed on Forever
> Forever splits Soulstone into the create spell (`Create Soulstone`) and the item (`/use Soulstone`). Press once to make the stone, press again to apply it to yourself or the hovered ally.

### Fear (CC — focus)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Fear
```

### Howl of Terror (AoE fear)
```lua
#showtooltip
/cast Howl of Terror
```

### Banish (demon/elemental CC)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Banish
```

### Death Coil (fear + self-heal)
```lua
#showtooltip
/cast Death Coil
```

### Eye of Kilrogg (scouting)
```lua
#showtooltip
/cast Eye of Kilrogg
```
> [!warning] Demonic Circle removed
> Demonic Circle (WotLK+) doesn't exist on Forever. Eye of Kilrogg is the classic warlock scouting tool — send your eye ahead to pull line of sight before a pull.

### Curse of Exhaustion (talent slow)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Curse of Exhaustion
```
> [!warning] Dark Pact removed
> Dark Pact (WotLK+) doesn't exist on Forever. Curse of Exhaustion (talent) is the classic kiting curse — big movement slow that pairs with Fear for control.

### Drain Mana (burn enemy mana)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Drain Mana
```

---

## 🛡️ Armors & Buffs

### Shadow Ward (shadow absorb)
```lua
#showtooltip
/cast Shadow Ward
```
> [!warning] Fel Armor removed
> Fel Armor (TBC+) doesn't exist on Forever. Shadow Ward is the classic anti-shadow buffer — great vs priest/shadow bosses. Demon Armor below is the default armor.

### Demon Armor (armor + health regen)
```lua
#showtooltip
/cast Demon Armor
```

### Detect Invisibility (utility)
```lua
#showtooltip
/cast Detect Invisibility
```

---

## 📋 Suggested Keybinds

| Key | Macro | Why |
|---|---|---|
| 1 | Shadow Bolt / Incinerate | Main nuke |
| 2 | Corruption / Immolate | DoT |
| 3 | Life Tap | Mana |
| 4 | Fear | CC |
| Q | Spell Lock | Interrupt |
| E | Death Coil | Self-heal |
| R | Healthstone | Survival |
| F | Banish | Demon CC |
| Shift-1 | Fel Domination | Instant summon |
| Mouse4 | Soulstone | Rez buff |

---

> [!note] Custom server check
> Forever is a Classic-era (level 60) client: no Haunt, Unstable Affliction, Seed of Corruption, Chaos Bolt, Metamorphosis, Immolation Aura, Demonic Empowerment, Demonic Circle, Dark Pact, Fel Armor, or Felguard — replaced with classic equivalents above (Curse of the Elements, Drain Life, Bane of Doom, Searing Pain, Fel Domination, Demonic Sacrifice, Health Funnel, Ritual of Summoning, Eye of Kilrogg, Curse of Exhaustion, Shadow Ward). Talent-gated buttons (Siphon Life, Conflagrate, Shadowburn, Incinerate, Curse of Exhaustion, Fel Domination, Demonic Sacrifice) grey out until you spend points. If a spell is greyed out or missing, check the Spellbook against the exact names above.