# WoW: Forever — Macro Library

Comprehensive macros for all 9 classes on the **WoW: Forever** server (Classic-era, max level 60, modern 12.1.5 engine — codename Camelot).

> [!important] Read this first: [00-Forever-Compatibility-Report.md](00-Forever-Compatibility-Report.md)
> The library was audited against Forever's real spell lists. Forever is **Classic 1.60.1 spells on a modern engine** — modern macro syntax works, but ~50 WotLK-era spell names were replaced with their Classic equivalents. The report documents everything that changed and why.

> [!info] What's in here
> - **00-Forever-Compatibility-Report.md** — the research + audit results (what works, what was replaced)
> - **01-Cross-Class.md** — universal macros that work on every class
> - **02-Warrior.md** … **10-Druid.md** — per-class macro packs
> - **11-Forever-Server-Specific.md** — macros for the server's custom systems (Legacy perk trees, Mana Well/Fermenter/Alchemy Lab recipes)
> - **12-Advanced-QoL.md** — hybrid buttons, priority chains, swap tricks (class-agnostic)
> - **13-Class-Extras.md** — second-layer per-class macros, each with a "why" note
> - **14-Raiding.md** — raid macros: leader tools, tank swaps, cooldown stacking, raid-duty macros
> - **15-Druid-Raid-and-Advanced.md** — advanced druid macros (Rake/Pounce/Lacerate/Primal Bite) with "why" notes
> - **16-Warrior-Stance-Weapon.md** — stance-dance + weapon-swap warrior pack (Charge/Intercept dance, Overpower dance, Execute big-weapon swap, tank panic button)
> - Every macro is verified against Forever's ability lists — no addons required, pure `/macro` commands

---

## How to Create a Macro

1. Press **`Esc` → Macros** (or `/macro`)
2. Click **New**, pick an icon, name it
3. Paste the macro text into the box
4. Drag the icon onto an action bar
5. Assign a keybind via **`Esc` → Key Bindings → Action Bar** (or bind inside the macro UI)

> [!warning] 255-character limit
> Each macro has a **255 character cap**. If a macro won't save, trim the comment lines or shorten spell names. All macros below are written to fit.

---

## Syntax Cheat Sheet (WotLK-era client)

| Condition | Meaning |
|---|---|
| `[mod:shift]` | Only while holding Shift (also `ctrl`, `alt`) |
| `[mod:shift,mod:alt]` | Hold **both** |
| `[combat]` / `[nocombat]` | In / out of combat |
| `[stealth]` | While stealthed (Rogue/Druid) |
| `[stance:1]` | While in stance/form #1 (Warrior stances, Druid forms) |
| `[harm]` / `[help]` | Target is hostile / friendly |
| `[dead]` / `[nodead]` | Target is dead / alive |
| `[@mouseover]` | Cast at hovered unit (fallback: target) |
| `[@focus]` | Cast at focus target |
| `[@player]` | Self-cast |
| `[exists]` | Unit exists |
| `nomod` / `noexists` / `noharm` | Negative versions |
| `#showtooltip` | Show the first spell's icon/tooltip |

**Structure:** `/cast [conditions] SpellName; [conditions2] Spell2`

The macro picks the **first** line/condition block that is valid. Semicolons separate fallbacks.

---

## Quick-Start: The 6 Macros Everyone Should Have

```lua
#showtooltip
/cast [mod:shift,@player] [@mouseover,help,nodead] [help,nodead] SpellName
```
*(mouseover-heal / shift-self pattern — replace SpellName with your heal)*

```lua
#showtooltip
/use 13
/use 14
```
*(Trinket slots — use both trinkets)*

```lua
#showtooltip
/cast [mod:shift,@player] [@mouseover,harm,nodead] [harm,nodead] SpellName
```
*(mouseover-harm pattern — interrupts/dots)*

```lua
/use [combat] Healthstone
/use [combat] Major Healing Potion
```
*(Combat potion: healthstone first, potion fallback)*

```lua
#showtooltip
/targetenemy [noharm][dead]
/startattack
```
*(Auto-target nearest enemy and start attacking)*

```lua
#showtooltip
/cast [@focus,harm,nodead][] SpellName
/focus [@focus,noexists]
```
*(Focus setup + cast-at-focus — first press sets focus, next casts)*

---

## Class Quick Links

| # | File | What It Adds |
|---|---|---|
| 1 | [01-Cross-Class.md](01-Cross-Class.md) | Universal QoL |
| 2 | [02-Warrior.md](02-Warrior.md) | Stance dancing, Charge/Intercept |
| 3 | [03-Paladin.md](03-Paladin.md) | Seals, Judgements, Blessings |
| 4 | [04-Hunter.md](04-Hunter.md) | Aspect juggling, pet control |
| 5 | [05-Rogue.md](05-Rogue.md) | Stealth openers, vanish tricks |
| 6 | [06-Priest.md](06-Priest.md) | Mouseover healing, dispels |
| 7 | [07-Shaman.md](07-Shaman.md) | Totem dropping, weapon buffs |
| 8 | [08-Mage.md](08-Mage.md) | Poly focus, spellsteal, blink |
| 9 | [09-Warlock.md](09-Warlock.md) | Life tap, soulstones, pet control |
| 10 | [10-Druid.md](10-Druid.md) | Form shifting, mouseover HoTs |
| 11 | [11-Forever-Server-Specific.md](11-Forever-Server-Specific.md) | **Legacy perks + custom recipes** |
| 12 | [12-Advanced-QoL.md](12-Advanced-QoL.md) | **Hybrid buttons, priority chains** |
| 13 | [13-Class-Extras.md](13-Class-Extras.md) | **Second-layer class macros + why** |
| 14 | [14-Raiding.md](14-Raiding.md) | **Raid macros: leader, tank swap, burst** |
| 15 | [15-Druid-Raid-and-Advanced.md](15-Druid-Raid-and-Advanced.md) | **Advanced druid: Savage Roar → Starfall** |

---

> [!tip] Custom server notes
> - Spell names below use standard WotLK names. If a custom talent renamed a spell on WoW: Forever, the macro will simply not fire — check the spell's exact name via the **Spellbook** and adjust.
> - **No addons required** — everything here is client-native `/macro` syntax.
> - PvP trinket / racial macros assume standard slots (13/14) — verify with `/script print(GetInventorySlotInfo("Trinket0Slot"))` if unsure.