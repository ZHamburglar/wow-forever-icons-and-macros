# Class Extras — New Macros + Why They Earn a Keybind

The original per-class files (02–10) covered the standard toolkit. This file adds **second-layer macros** — combo openers, panic buttons, execute/swap tricks — with a **"Why"** note on every one so you know what it buys you before you bind it.

> [!info] How to read the "Why" notes
> Each macro below is followed by a `> [!tip] Why it's useful` callout. If the reason doesn't match your playstyle (PvE vs PvP, tank vs DPS), skip it — these are optional power-ups, not required rotation.

---

# ⚔️ Warrior Extras

### Sunder Armor Stacker (tank opener)
```lua
#showtooltip
/castsequence reset=target Sunder Armor, Sunder Armor, Sunder Armor, Sunder Armor, Sunder Armor
```
> [!tip] Why it's useful
> Tanking requires 5 Sunder stacks for threat + armor shred. This button auto-cycles through them and **resets when you switch targets** — you never manually track which stack you're on. One key, perfect threat opener.

### Stance-Smart Shield Bash (any stance)
```lua
#showtooltip
/cast [stance:2] Shield Bash; [stance:1,harm] Shield Bash
```
> [!tip] Why it's useful
> Shield Bash only works in Defensive stance. This macro **auto-swaps to Defensive** (line 1) then bashes — one press, no stance dance first. Interrupts land even mid-rotation in Battle stance.

### Execute + Weapon Swap (2H slam)
```lua
#showtooltip
/equipslot 16, Sulfuras, the Extinguished Hand
/cast Execute
```
> [!tip] Why it's useful
> Warriors often tank with 1H+Shield then swap to 2H for Execute phases. This macro swaps the weapon AND fires Execute in one press — no wasted GCD fumbling gear mid-fight.

### Panic Button (Shield Wall + Last Stand + Pot)
```lua
#showtooltip
/cast Shield Wall
/cast Last Stand
/use [combat] Major Healing Potion
```
> [!tip] Why it's useful
> When you're about to die, you don't have time for three separate keys. This one button: damage reduction + max-HP boost + potion. Press it, survive, live to fight the next pull.

---

# 🛡️ Paladin Extras

### Seal Dancer (swap seal on the fly)
```lua
#showtooltip
/cast [mod:shift] Seal of Command; [mod:ctrl] Seal of Righteousness; Seal of the Crusader
```
> [!tip] Why it's useful
> Different seals for different fights: Command (2H burst, talent), Righteousness (fast 1H), Crusader (increases Holy damage + crit on Judgement). One button swaps between the three. **Seal of Vengeance doesn't exist in Forever** — Crusader replaces it.

### Tank Pull (Righteous Fury + Consecration)
```lua
#showtooltip
/cast Righteous Fury
/cast Consecration
```
> [!tip] Why it's useful
> Opens a tank pull correctly: threat buff up + ground AoE down. Two actions that belong together, one key — so you never forget Righteous Fury on pull #1 and lose aggro.

### Hand of Sacrifice / Freedom combo
```lua
#showtooltip
/cast [@focus,help,nodead] Blessing of Sacrifice; [@mouseover,help,nodead] Blessing of Freedom
```
> [!tip] Why it's useful
> Focus = tank you're saving (Sacrifice redirects damage), mouseover = anyone rooted (Freedom breaks it). One button, two lifesaving blessings. **Forever uses Classic naming — these are Blessing of Sacrifice/Freedom, not Hand of Sacrifice/Freedom.**

### Holy Shock Rescue (save anyone)
```lua
#showtooltip
/cast [@mouseover,help,nodead] Holy Shock; [@player] Holy Shock
```
> [!tip] Why it's useful
> Instant 3k+ burst heal on whoever you hover — faster than any cast-time heal. Hover the dying DPS, press, done. Self-casts when no mouseover so it doubles as your own emergency.

---

# 🏹 Hunter Extras

### Trap + Trap Launcher (stay safe)
```lua
#showtooltip
/cast [mod:shift] Explosive Trap; [mod:ctrl] Freezing Trap; Frost Trap
```
> [!tip] Why it's useful
> One key, three traps: Shift = damage (Explosive), Ctrl = hard CC (Freezing), plain = slow (Frost). You never waste a GCD fumbling the wrong trap into the wrong fight.

### Pet Re-Zero (dismiss + resummon fresh)
```lua
#showtooltip
/cast Dismiss Pet
/cast Call Pet
```
> [!tip] Why it's useful
> Resets your pet's position, aggro, and buffs instantly — perfect after a wipe, a pet death, or a bad pull where your pet is in the wrong spot. One press re-zeros everything.

### Bestial Wrath + Pet Attack (clean threat)
```lua
#showtooltip
/cast [@focus,harm,nodead][] Bestial Wrath
/petattack
```
> [!tip] Why it's useful
> **Misdirection doesn't exist in Forever** (it's a TBC+ spell) — threat control comes from Bestial Wrath + pet attack timing instead. This fires your pet's burst and sends it in, one key.

### Deterrence + Feign Death (oh-sheet button)
```lua
#showtooltip
/cast Deterrence
/cast Feign Death
```
> [!tip] Why it's useful
> Parry-everything + drop-aggro in one key. When a mob peels off the tank at you, this button saves your life — the two best hunter defensives firing together.

---

# 🗡️ Rogue Extras

### Shadowstep + Ambush (stealth opener)
```lua
#showtooltip
/cast [stealth] Ambush; [nostealth] Backstab
```
> [!tip] Why it's useful
> **Shadowstep doesn't exist in Forever** (TBC+). The classic stealth opener is Ambush (huge burst from stealth); out of stealth the same key falls back to Backstab. One key, always the right opener — no retargeting, no stance juggling.

### Vanish + Gouge (get-out-of-jail)
```lua
#showtooltip
/cast Vanish
/cast Gouge
```
> [!tip] Why it's useful
> Vanish drops combat/aggro; Gouge (4s stun) locks the mob in place while you reposition. The classic Rogue escape — one key instead of two frantic presses.

### Cold Blood + Rupture (guaranteed crit DoT)
```lua
#showtooltip
/cast Cold Blood
/cast Rupture
```
> [!tip] Why it's useful
> Cold Blood guarantees your next finisher crits — pairing it with Rupture (a DoT) means the crit applies to the *whole* DoT, not one hit. More damage per combo point than critting Eviscerate.

### Pick Pocket + Stealth Loop (farm)
```lua
#showtooltip
/cast Pick Pocket
/cast Stealth
```
> [!tip] Why it's useful
> Auto-stealth after pickpocketing — instant repeat for loot farming humanoid mobs. Gold + reagents without ever leaving stealth.

---

# 💒 Priest Extras

### Inner Focus + Greater Heal (free big heal)
```lua
#showtooltip
/cast Inner Focus
/cast [@mouseover,help,nodead][@player] Greater Heal
```
> [!tip] Why it's useful
> Inner Focus makes your next spell free + crit-boosted. Locking it onto Greater Heal means every 3-min button press = a free, huge, guaranteed-crit heal. Best mana-efficiency trick in the kit.

### Shield + Renew (tank bubble macro)
```lua
#showtooltip
/cast [@focus,help,nodead] Power Word: Shield
/cast [@focus,help,nodead] Renew
```
> [!tip] Why it's useful
> Two HoTs/bubbles on the tank (focus) in one key — the Disc priest's "keep the MT alive" button. Hover anyone else for the same combo on them.

### Shadow Word: Death (execute)
```lua
#showtooltip
/cast [@mouseover,harm,nodead][] Shadow Word: Death
```
> [!tip] Why it's useful
> The shadow execute — massive damage on low-HP targets. Mouseover-first so you snipe dying adds without losing your main target.

### Fade (threat dump)
```lua
#showtooltip
/cast Fade
```
> [!tip] Why it's useful
> The healer's threat-dump — one press drops a chunk of aggro. Bind it somewhere you can hit *instantly* when a mob peels; healers who don't have this keyed die to adds.

---

# 🌩️ Shaman Extras

### Riptide + Chain Heal (tank-top-up)
```lua
#showtooltip
/cast [@mouseover,help,nodead] Riptide
/cast [@mouseover,help,nodead] Chain Heal
```
> [!tip] Why it's useful
> Riptide's HoT then a Chain Heal that jumps to nearby raid members — the resto shaman's "heal the tank AND the group" button. One press, one hover.

### Elemental Mastery + Trinket (shaman raid burst)
```lua
#showtooltip
/cast Elemental Mastery
/use 13
```
> [!tip] Why it's useful
> **Bloodlust and Fire Elemental Totem don't exist in Forever** (Classic-era Shaman has no lust). The classic burst is Elemental Mastery (talent): your next Lightning Bolt becomes instant, guaranteed crit, +20% damage. Stack it with a trinket proc for the raid burst window. One key when the raid leader calls for burst.

### Purge Priority (interrupt + dispel)
```lua
#showtooltip
/cast [@focus,harm,nodead] Purge; [@mouseover,harm,nodead] Purge; [harm] Purge
```
> [!tip] Why it's useful
> Enemy buffs stripped in focus-priority order — the shaman's hardest counter to paladins/mages. One key always purges the *right* target without retargeting.

### Totem Re-Zero (recall + redrop)
```lua
#showtooltip
/cast Totemic Recall
```
> [!tip] Why it's useful
> Recalls all four totems and refunds some mana — use before a boss moves or a fight ends so you can redrop fresh totems with full mana. *(WotLK ability — if your tree lacks it, skip.)*

---

# ❄️ Mage Extras

### Nova + Blink (escape root)
```lua
#showtooltip
/cast Frost Nova
/cast Blink
```
> [!tip] Why it's useful
> Freeze everything around you (8s root) then blink away — the mage's "melee are on me" button. One key separates you from danger completely.

### Full Burst (Arcane Power + Presence + Trinket)
```lua
#showtooltip
/cast Arcane Power
/cast Presence of Mind
/use 13
```
> [!tip] Why it's useful
> The mage burn window in one key: +30% damage, instant next cast, trinket proc. Pop it when the boss hits 35% and watch the parse. *(Replace trinket slot if yours is 14.)*

### Counterspell + Remove Lesser Curse (defensive purge)
```lua
#showtooltip
/cast [mod:shift] Remove Lesser Curse; [@focus,harm,nodead] Counterspell
```
> [!tip] Why it's useful
> Two of the mage's best tools on one key: plain = interrupt your focus, Shift = remove a curse off whoever you're targeting. **Spellsteal doesn't exist in Forever** (TBC+) — Remove Lesser Curse is the classic defensive.

### Ice Block Toggle (self-freeze + cancel)
```lua
#showtooltip
/cast Ice Block
```
> [!tip] Why it's useful
> Press to freeze yourself immune; press the **same button again while frozen** (with a `/cancelaura Ice Block` on the second line in your second macro) to thaw early. Bind both macros to the same key and you control the block duration.

---

# 💀 Warlock Extras

### Life Tap + Healthstone (safe mana)
```lua
#showtooltip
/cast Life Tap
/use [combat] Healthstone
```
> [!tip] Why it's useful
> Life Tap trades health for mana; the healthstone instantly refunds that health. One key = mana refill with zero downtime — the sustain trick that keeps locks grinding forever.

### Soulstone the Tank (auto-rez)
```lua
#showtooltip
/cast [@focus,help,nodead] Create Soulstone; [@mouseover,help,nodead] Create Soulstone
/use [@focus,help,nodead] Soulstone
```
> [!tip] Why it's useful
> Focus = tank, mouseover = anyone else. One key creates AND applies the rez-buff to the right person before every pull — you never wipe the raid because the MT lacked a soulstone.

### Banish / Fear (demon vs humanoid)
```lua
#showtooltip
/cast [@focus,harm,nodead] Banish
/cast [@focus,harm,nodead] Fear
```
> [!tip] Why it's useful
> Banish locks demons/elementals; Fear locks humanoids. Both on your focus — one key always applies the *right* CC for the target type. The warlock's CC answer to everything.

### Demonic Circle (place + teleport)
```lua
#showtooltip
/cast [mod:shift] Subjugate Demon; Eye of Kilrogg
```
> [!warning] Demonic Circle removed
> Demonic Circle is WotLK-era and doesn't exist in Forever. The classic warlock utility replacements: **Eye of Kilrogg** (scout) and **Subjugate Demon** (control a demon, then release). Use those for the same "set up before the fight, escape after" role.

---

# 🐻 Druid Extras

### Form-Dance Opener (prowl + ravage + FF)
```lua
#showtooltip
/cast [nostealth] Prowl
/cast [stealth] Ravage
/cast [stealth] Faerie Fire
```
> [!tip] Why it's useful
> The full feral opener on one key: stealth → Ravage (bonus damage from stealth) → Faerie Fire (armor shred) — all while still stealthed. You start the fight with your biggest hit *and* the debuff applied.

### Shift-Cancel + Instant Rejuv (heal out of form)
```lua
#showtooltip
/cast [nostance:3] Cat Form
/cast [stance:3] Rejuvenation
```
> [!tip] Why it's useful
> Rejuvenation is instant and keeps ticking in cat form. This shifts out, HoTs you, and you can shift back — **no cast time wasted** vs Healing Touch. The leveling heal that doesn't stop your DPS.

### Bear Panic (Enrage + Frenzied Regeneration)
```lua
#showtooltip
/cast Enrage
/cast [@player] Frenzied Regeneration
```
> [!tip] Why it's useful
> Frenzied Regen heals based on rage — Enrage just filled your rage bar. Press both: instant big self-heal with max rage conversion. The bear's "I'm dying" button.

### Root + Hibernate (lockdown combo)
```lua
#showtooltip
/cast [mod:shift] Hibernate; Entangling Roots
```
> [!tip] Why it's useful
> Roots pin a target in place (melee), Hibernate puts a beast to sleep (hard CC). Plain = root the current target, Shift = hibernate your focus. **Cyclone doesn't exist in Forever** (TBC+) — Hibernate is the classic druid hard CC for beasts. Two CC tools, one key.

---

## 📋 Quick Pick Chart

| Class | #1 New Macro | Why |
|---|---|---|
| Warrior | Sunder stacker | Auto threat opener |
| Paladin | Seal dancer | Right seal per fight |
| Hunter | Trap selector | 3 traps, 1 key |
| Rogue | Stealth opener | Instant Ambush from stealth |
| Priest | Inner Focus+Greater Heal | Free crit big heal |
| Shaman | Riptide+Chain Heal | Tank+group in one |
| Mage | Nova+Blink | Melee escape |
| Warlock | Life Tap+Healthstone | Infinite sustain |
| Druid | Form-dance opener | Full feral opener |

---

> [!note] Compatibility
> All macros use WotLK-era syntax (the Forever client build). If a spell name differs due to custom talents, swap in your Spellbook's exact name — the pattern is what makes these macros powerful.