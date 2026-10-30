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
> [!tip] Why it's valuable
> Corruption is your core damage-over-time — one press from the mouseover keeps it rolling on the target without switching your selection, so your filler (Shadow Bolt) never pauses.

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
> [!tip] Why it's valuable
> The warlock's bread-and-butter filler — every GCD not spent on a DoT, curse, or cooldown goes here. A dedicated key keeps the rotation honest.

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
> [!tip] Why it's valuable
> The Affliction execute — big damage on sub-25% targets AND it fills your soul shard bag so your next summon/stone costs nothing. One key for the whole last phase.

### Siphon Life (talent DoT — self-heal)
```lua
#showtooltip
/cast Siphon Life
```
*(Talented in Affliction — greyed out until you spend points.)*
> [!tip] Why it's valuable
> A DoT that also heals you every tick — free sustain on every target you fight. The talent-gated note is there because it greys out until you spend Affliction points.

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
> [!tip] Why it's valuable
> Your single-target damage curse — it ramps up over 24s, so the earlier it's on, the more total damage it does. Mouseover keeps it applied without breaking your cast target.

---

## 🔥 Destruction

### Incinerate (talent nuke)
```lua
#showtooltip
/cast Incinerate
```
*(Incinerate is a Destruction talent on Forever — take it before keybinding.)*
> [!tip] Why it's valuable
> The Destruction nuke that fires fast and hits hard — and it benefits from your Immolate DoT. Talented-only, so it's greyed out until you invest.

### Immolate (DoT + Conflagrate fuel)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][harm] Immolate
```
> [!tip] Why it's valuable
> Fire DoT that does damage now AND unlocks Conflagrate's burst — keeping it up is the Destruction rotation's first rule.

### Conflagrate (talent burst after Immolate)
```lua
#showtooltip
/cast Conflagrate
```
> [!tip] Why it's valuable
> Instant burst that consumes Immolate's remaining ticks — the Destruction burst window in one press, no channel, no cast bar.

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
> [!tip] Why it's valuable
> Instant-cast execute for Destruction — sub-25% targets die instantly and it refunds a soul shard on kill. The "pop it at 20%" button.

### Soul Fire (long-cast nuke)
```lua
#showtooltip
/cast Soul Fire
```
> [!tip] Why it's valuable
> Your biggest single hit — long cast, but it's the Demonology nuke that makes the burst window count. Bind it where you won't need to move for 3 seconds.

### Rain of Fire (AoE)
```lua
#showtooltip
/cast Rain of Fire
```
> [!tip] Why it's valuable
> The warlock's AoE — ground-targeted fire rain that burns everything in the zone. One key for trash packs and adds.

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
> [!tip] Why it's valuable
> Channels health to your pet — the keep-the-Voidwalker-alive button on tanking duty. Mouseover-safe so you never drop target.

### Ritual of Summoning (summon a party member)
```lua
#showtooltip
/cast Ritual of Summoning
```
> [!warning] Summon Felguard removed
> Summon Felguard (TBC+) doesn't exist on Forever — classic pets are Imp, Voidwalker, Succubus/Incubus, Felhunter. Ritual of Summoning is the classic utility that pulls a party member straight to you.
> [!tip] Why it's valuable
> Pulls a group member straight to you — the classic "summon the healer from the entrance" raid utility. Costs a soul shard, saves a 10-minute walk.

---

## 🐾 Pet Management

### Pet Attack (+ weapon swing)
```lua
#showtooltip
/petattack
/startattack
```
*(Classic pets have no Kill Command; add the pet's situational spell per encounter: Torment, Seduction, Devour Magic, Spell Lock.)*
> [!tip] Why it's valuable
> Sends your pet in and starts your own melee swing — the classic "everything engages at once" button. No Kill Command on Forever, so this is the pet DPS base.

### Pet Follow
```lua
/petfollow
```
> [!tip] Why it's valuable
> Recalls your pet out of danger — one press when it's eating AoE or pulling adds. Every warlock needs this bound; it's the difference between a dead pet and a live one.

### Pet Passive
```lua
/petpassive
```
> [!tip] Why it's valuable
> Stops your pet attacking immediately — the leash for when a fight isn't yours yet. Prevents accidental pulls in dungeons.

### Succubus Seduce (CC)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Seduction
```
> [!tip] Why it's valuable
> Your Succubus's hard CC — 15-second seduce on humanoids. Focus-based so you control the assigned add without retargeting, exactly like a mage's Polymorph duty.

### Felhunter Devour Magic (dispels enemy buffs)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Devour Magic
```
> [!tip] Why it's valuable
> Your Felhunter eats an enemy buff (or removes a debuff from an ally) — the warlock's dispel, on a pet. Focus-based = strip the boss's shield without breaking your rotation.

### Felhunter Spell Lock (interrupt)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Spell Lock
```
> [!tip] Why it's valuable
> Your Felhunter's interrupt — the warlock's answer to caster mobs. Focus-targeted so the assigned cast always gets locked down.

### Voidwalker taunt
```lua
#showtooltip
/cast [@focus,harm,nodead][] Suffering
```
> [!tip] Why it's valuable
> Your Voidwalker's taunt — the pet tank's threat button. Focus-based so the VW grabs the add you designate, buying you time to re-CC or burst.

### Pet Summon Quick-Switch
```lua
#showtooltip
/cast [mod:shift] Summon Voidwalker; [mod:ctrl] Summon Succubus; [mod:alt] Summon Felhunter; Summon Imp
```
*(Shift=VW, Ctrl=Succubus, Alt=Felhunter, default=Imp — classic pets only, no Felguard.)*
> [!tip] Why it's valuable
> Swap pets by modifier — Shift=VW (tank), Ctrl=Succubus (CC), Alt=Felhunter (dispel/interrupt), default=Imp (dps). One key swaps your whole toolkit for the situation.

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
> [!tip] Why it's valuable
> Makes and eats a healthstone in one press — the warlock's personal emergency heal. Always have one made; this key both creates and consumes.

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
> [!tip] Why it's valuable
> Your primary hard CC on humanoids — focus-based so the assigned target stays feared while you DPS the main kill. The warlock's "hold the add" button.

### Howl of Terror (AoE fear)
```lua
#showtooltip
/cast Howl of Terror
```
> [!tip] Why it's valuable
> Fears everything around you — the get-out-of-jail button when adds swarm you. Costs a soul shard, saves your life.

### Banish (demon/elemental CC)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Banish
```
> [!tip] Why it's valuable
> Locks demons and elementals out of the fight entirely — the CC for the enemy types Fear can't touch. Focus-based for assigned-CC duty.

### Death Coil (fear + self-heal)
```lua
#showtooltip
/cast Death Coil
```
> [!tip] Why it's valuable
> The warlock's panic button — fears the target AND heals you for a chunk. One key that both saves you and controls the enemy.

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
> [!tip] Why it's valuable
> Big movement slow on your focus — the kiting tool that pairs with Fear: fear them, slow them, out-run them. Talented in Affliction first.

### Drain Mana (burn enemy mana)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Drain Mana
```
> [!tip] Why it's valuable
> Drains a caster's mana into yours — the anti-healer/caster tool that wins the long fight. Focus-based so you can drain the boss while DoTs tick.

---

## 🛡️ Armors & Buffs

### Shadow Ward (shadow absorb)
```lua
#showtooltip
/cast Shadow Ward
```
> [!warning] Fel Armor removed
> Fel Armor (TBC+) doesn't exist on Forever. Shadow Ward is the classic anti-shadow buffer — great vs priest/shadow bosses. Demon Armor below is the default armor.
> [!tip] Why it's valuable
> Soaks shadow damage — the pre-fight buffer vs priests and shadow bosses. One press before the pull makes the opening hits free.

### Demon Armor (armor + health regen)
```lua
#showtooltip
/cast Demon Armor
```
> [!tip] Why it's valuable
> Your default armor — armor AND health regen in one buff. The 30-minute buff you re-apply after every death and wipe.

### Detect Invisibility (utility)
```lua
#showtooltip
/cast Detect Invisibility
```
> [!tip] Why it's valuable
> Reveals stealthed targets — the anti-rogue/anti-camper tool. Worth a niche bind for world PvP and stealth-heavy dungeons.

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