# 🧙 WoW: Forever — Icons & Macros

A curated toolkit for **World of Warcraft: Forever** — the new Classic-era evolution of WoW (max level 60, 9 classes, codename *Camelot*). This repo holds two things we built and maintain:

1. 🖼️ **A 33k-icon library** — every ability/class/profession icon, organized and searchable
2. ⌨️ **A 426-macro library** — per-class macro packs, every one with a "why it's valuable" explanation

> [!NOTE]
> **Forever is a Classic-era game on a modern engine.** That means modern macro *syntax* works (`[mod:shift]`, `[@mouseover]`, `/castsequence`…), but the *spells* are Classic 1.60.1 — no Bloodlust, no Mangle, no Cyclone. Everything here was verified against Forever's real ability lists, so you won't find dead macros.

---

## 🖼️ Part 1 — Icon Library (`icons/`)

**33,193 icons** pulled from Wowhead's CDN, named with their exact game filenames (e.g. `inv_sword_36.jpg`) so they drop straight into addon/UI work.

| Category | Icons | Contents |
|---|---|---|
| ⚔️ `Classes/` | 1,395 | All 13 classes (Druid, Hunter, Mage, Warrior…) |
| 🧵 `Professions/` | 2,873 | All 14 professions (Alchemy, Blacksmithing, Herbalism…) |
| 📦 `General/` | 28,925 | Abilities, Achievements, Items, Mounts, Pets, Spells, UI, Races, PvP… |

**How to browse it:** open `icons/index.html` in any browser — searchable gallery with category tabs; click any icon to copy its filename. Zip bundles of each category sit alongside the folders for bulk download.

---

## ⌨️ Part 2 — Macro Library (`macros/`)

**426 macros** across 15 files, written for Forever's real spell set and formatted for Obsidian. **Every single macro carries a `> [!tip] Why it's valuable` explanation** — what it does *and* why it earns a keybind.

| File | What's inside |
|---|---|
| `00-Forever-Compatibility-Report.md` | The research: Forever's engine, ~50 WotLK spells that don't exist, and every replacement made |
| `01-Cross-Class.md` | Universal QoL: mouseover heals, focus CC, trinket/racial burst, hybrid buttons |
| `02-Warrior.md` → `10-Druid.md` | Per-class packs (9 classes) — includes advanced kits (warrior stance-dance + weapon-swap, druid raid pack) |
| `11-Forever-Server-Specific.md` | Forever's custom systems: Legacy perk trees, Mana Well/Fermenter/Alchemy recipes |
| `12-Advanced-QoL.md` | Priority chains, target-of-target assist, weapon-swap tricks (any class) |
| `13-Class-Extras.md` | Second-layer per-class macros |
| `14-Raiding.md` | Raid leader tools, tank-swap taunts, cooldown stacking, raid-duty macros |

**How to use:** `/macro` → New → paste → drag to bar. Pure `/macro` commands — **no addons required**, and all macros fit the 255-character limit.

---

## 📁 Repo Layout

```
wow-forever-icons-and-macros/
├── README.md               ← you are here
├── icons/                  ← 33,193 icons
│   ├── Classes/            ← 13 class folders (1,395 icons)
│   ├── Professions/        ← 14 profession folders (2,873 icons)
│   ├── General/            ← 15 categories, 400+ subfolders (28,925 icons)
│   ├── index.html          ← searchable visual gallery (click-to-copy names)
│   └── README.md           ← icon library details + full category table
└── macros/                 ← 426 macros, all explained
    ├── 00-Forever-Compatibility-Report.md
    ├── 01-Cross-Class.md
    ├── 02-Warrior.md … 10-Druid.md
    ├── 11-Forever-Server-Specific.md
    ├── 12-Advanced-QoL.md
    ├── 13-Class-Extras.md
    ├── 14-Raiding.md
    └── README.md           ← macro library details, syntax cheat sheet, keybinds
```

---

## 🛠️ How it was built (the short version)

- **Icons:** enumerated Wowhead's icon list via the Wago API, downloaded every image from Zamimg's CDN, then categorized 33k files into Classes / Professions / General with an automated pipeline (scripts live in the repo history — `wago_fetch.py`, `categorize.py`, `make_index.py`).
- **Macros:** written for the 9 Forever classes, then **audited against Forever's real ability+talent lists** (parsed from Warcraft Wiki). The audit flagged ~50 WotLK-era spells that don't exist in Forever — each was replaced with its Classic equivalent (Bloodlust → Elemental Mastery, Misdirection → Bestial Wrath, Cyclone → Hibernate, etc.). Zero dead macros, and talent-gated spells are marked `(talent)` so you know which need points spent.

---

## 📝 Notes

- Icons are 56×56 JPG (WoW's standard icon size), named exactly as the game references them.
- Macros reference **placeholder weapon names** in the swap macros — swap in your actual gear.
- Forever's custom talents may rename a spell here or there; `#showtooltip` in every macro shows what's bound, making any mismatch self-debugging.

Enjoy — and may your dps meters be green. 🟢