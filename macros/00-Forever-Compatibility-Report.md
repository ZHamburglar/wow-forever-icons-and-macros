# WoW: Forever Macro Compatibility — Research Findings

**Date:** 2026-10-29 · **Audit of all 15 macro files against Forever's real spell lists**

---

## 1. What WoW: Forever actually is (the big discovery)

> [!warning] The library was originally written for the wrong game!
> The first 10 files assumed a **WotLK-era client** with WotLK spell names. Research shows **WoW: Forever is a new evolution of WoW Classic** — max level 60, 9 classes, Classic 1.60.1 spell sets — running on the **modern (12.1.5) engine**. That means:
> - ✅ **Macro syntax is MODERN** — all conditionals work: `[mod:shift]`, `[@mouseover]`, `[@focus]`, `[harm]`/`[help]`, `/castsequence`, `#showtooltip`, `/equipslot`, `SetRaidTarget`, `/readycheck`, `SendChatMessage` scripts.
> - ❌ **Spell NAMES are CLASSIC 1.60.1** — ~50 WotLK-era spells used in the library **do not exist**: no Bloodlust, no Tiger's Fury, no Savage Roar, no Spellsteal, no Misdirection, no Guardian Spirit, no Cyclone, no Metamorphosis, no Fan of Knives…

**Sources:**
- Blizzard official page: `worldofwarcraft.blizzard.com/en-us/forever` — "World of Warcraft: Forever", launches Nov 4, 2026
- Wowhead Forever branch: `wowhead.com/forever` — Patch 1.60.1 guides
- Warcraft Wiki: `warcraft.wiki.gg/wiki/World_of_Warcraft:_Forever` — Classic+ (codename Camelot), modern engine
- Patch notes: `Patch 1.60.1/API_changes/notes` — *"Forever shares Mainline WoW's UI architecture, including the vast majority of APIs available in 12.1.5"*

## 2. What changed (verified against per-class ability lists)

### Macro SYSTEM: everything modern works
| Feature | Works? | Source |
|---|---|---|
| `[mod:shift/ctrl/alt]` conditionals | ✅ | modern engine |
| `[@mouseover]`, `[@focus]`, `[@focustarget]`, `[@targettarget]` | ✅ | modern engine |
| `/castsequence`, `#showtooltip`, `/focus`, `/clearfocus` | ✅ | modern engine |
| `/equipslot`, `/equipset` (Equipment Manager) | ✅ | modern engine |
| `SetRaidTarget` mark scripts, `/readycheck` | ✅ | modern engine |
| `/script` Lua (SendChatMessage, RepairAllItems, UnitName) | ✅ | modern engine (macros = hardware events) |
| 255-char macro limit | ✅ | applies to all |
| Addons | ✅ | TOC game type `forever`/`camelot`, WOW_PROJECT_ID=18 |

### SPELLS: ~50 dead across the library (all fixed in v2)
| Class | Removed (WotLK-era, doesn't exist in Forever) | Replaced with |
|---|---|---|
| Warrior | Spell Reflection | Shield Block + Disarm |
| Paladin | Avenger's Shield, Hammer of the Righteous, Divine Plea, Righteous Defense, Hand of Protection/Freedom/Sacrifice, Judgement, Turn Evil, Shield of Righteousness | Blessing of Protection/Freedom/Sacrifice, Judgment, Turn Undead, Holy Shield (talent) |
| Hunter | Steady Shot, Kill Command, Explosive Shot, Chimera Shot, Misdirection, Silencing Shot, Tranquilizing Shot, Aspect of the Viper | Bestial Wrath (talent), classic shots |
| Rogue | Envenom, Fan of Knives, Killing Spree, Cloak of Shadows, Shadowstep, Dismantle | Ambush/Backstab opener, Detect Traps |
| Priest | Circle of Healing, Guardian Spirit, Lightwell, Mass Dispel, Mind Sear | Prayer of Healing, Holy Nova (talent), PW:S |
| Shaman | **Bloodlust**, Earth Shield, Cleanse Spirit, Feral Spirit, Fire Elemental Totem, Lava Lash, Thunderstorm, Wrath of Air Totem | Elemental Mastery (talent), Grace of Air Totem, Mana Tide (talent) |
| Mage | Summon Water Elemental, Deep Freeze, Living Bomb, Dragon's Breath, Invisibility, Mirror Image, Create Mana Gem, Molten Armor, Spellsteal | Conjure Mana Ruby, Remove Lesser Curse |
| Warlock | Haunt, Seed of Corruption, Chaos Bolt, Metamorphosis, Immolation Aura, Demonic Empowerment, Summon Felguard, Demonic Circle, Dark Pact, Fel Armor, Curse of Agony, Unstable Affliction | Demon Armor, Bane of Agony, Create Soulstone |
| Druid | Mangle, Tiger's Fury, Survival Instincts, Cyclone, Flight Form, Force of Nature, Lifebloom, Savage Roar, Maim, Starfall, Tree of Life | Rake, Pounce (36), Primal Bite (talent), Lacerate (42), Dire Bear Form (40), Hibernate, Soothe Animal |

### KEY CLASSIC-ERA SUBSTITUTIONS (Forever uses these instead)
- **No Bloodlust/Heroism** — Shaman burst = Elemental Mastery (talent), instant crit Lightning Bolt
- **No Misdirection** — Hunter threat control = Bestial Wrath (talent) + pet timing
- **No Spellsteal** — Mage dispel duty = Remove Lesser Curse
- **No Guardian Spirit** — Priest tank-save = pre-cast Power Word: Shield
- **No Cyclone** — Druid hard CC = Hibernate (beasts)
- **No Tiger's Fury / Mangle / Savage Roar** — Classic feral = Claw/Rake/Shred → Rip/Ferocious Bite, Primal Bite talent; bear = Maul/Lacerate
- **No Create Mana Gem** — classic gems = Conjure Mana Agate/Jade/Citrine/Ruby

## 3. Verification method

- Parsed all 9 per-class Forever ability+talent tables from Warcraft Wiki → `/home/burgeragentpc/wow-macros/forever_ground_truth.json`
- Ran a spell-name audit script over every `/cast` line in all 13 files
- Classified: OK / TALENT (works if talented — noted in the macro) / RENAMED (fixed) / DEAD (removed)
- **Consolidation (2026-10-29):** the standalone druid expansion and warrior stance/weapon packs were merged into `10-Druid.md` and `02-Warrior.md` respectively — one file per class, everything verified after the merge (0 dead spells)
- Cross-class files (01, 12, 14) checked against the union of all ability+talent lists

## 4. Remaining caveats (honest)

- **Talent-gated macros**: several macros use spells that only exist as *talents* (e.g. Bestial Wrath, Elemental Mastery, Holy Shield, Primal Bite, Insect Swarm, Moonkin Form, Berserk, Swiftmend, Wild Growth). They're marked "(talent)" in the files — a player without the talent gets a dead button. This is inherent to Forever's talent design.
- **Custom items** (Mana Well, Fermenter, Lich's Index Finger) and **Legacy perk** macros in file 11 are based on the server's custom content — item names should be verified against the actual game.
- **Racial names** are Classic: Orc Blood Fury, Troll Berserking, Tauren War Stomp, Undead Will of the Forsaken — the cross-class racial burst macro was updated to use these.
- If a spell still doesn't fire in-game, check the **Spellbook** for the exact name — Forever's custom talents may rename spells. `#showtooltip` shows what's bound, making it self-debugging.