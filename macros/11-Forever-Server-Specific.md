# WoW: Forever — Server-Specific Macros

These macros are unique to **WoW: Forever** — they exploit the server's custom systems: the **Legacy perk trees** (Adventure, Professions, Resourcefulness) and the **custom profession recipes** (Mana Well, Fermenter, Alchemy Laboratory, Lich's Index Finger, etc.).

> [!info] Why these macros exist
> Standard WotLK macro guides don't cover Forever's custom systems. These macros turn Legacy perks and custom recipes into one-button actions — exactly what the leveling guide's "self-sufficiency" strategy wants.

---

## 🎒 Legacy: Adventure Tree

### Field Medicine → Super Bandage (self)
```lua
#showtooltip
/use [@player] Heavy Runecloth Bandage
```
> [!tip] Why it's useful
> With **Field Medicine (2/2)** your bandages heal ~50% more. A one-button self-bandage is your cheapest emergency heal while leveling — no mana, no cooldown beyond the bandage timer. The `[@player]` guarantees it targets *you*, never a mouseover mob.

### Field Medicine + Poison Cure combo (bandage then cure)
```lua
#showtooltip
/cast [@player] Abolish Poison
/use [@player] Heavy Runecloth Bandage
```
> [!tip] Why it's useful
> Poison + low HP is the #1 leveling death. One key: strip the poison, then bandage. **Field Medicine** also boosts bandage healing, so this combo is your "get out of dying" button on classes without self-heals (Warrior, Rogue).

### Field Guide → Quest Item Quick-Use
```lua
#showtooltip
/use [@cursor] Quest Item
```
> [!tip] Why it's useful
> **Field Guide** improves quest tracking — and many Forever quests are "use item on thing" quests. This drops the quest item at your cursor position in one click instead of fishing it out of your bags. *(Replace "Quest Item" with the actual item name — hover it in your bag.)*

---

## 🍲 Legacy: Professions Tree

### Master Chef → Eat + Drink in one key
```lua
#showtooltip
/use [nomod] Grilled Grouper
/use [mod:shift] Filtered Draenic Water
```
> [!tip] Why it's useful
> **Master Chef** makes food stronger/cheaper to craft; **Bountiful Harvest** multiplies cooking yields. Leveling = constant eating. One button: plain press eats, Shift+press drinks — no bag hunting mid-grind.

### Bountiful Harvest → Cook + Eat loop
```lua
#showtooltip
/use [nomod] Grilled Grouper
/use [mod:shift] Filtered Draenic Water
```
> [!tip] Why it's useful
> **Cooking is a tradeskill, not a /castable spell** in Forever — there's no `/cast Cooking`. Keep the tradeskill window's Cook button for crafting (with **Bountiful Harvest** doubling yields), and use this one key for the eat/drink side: plain = eat, Shift = drink, no bag hunting mid-grind.

### Fermenter / Alchemy Laboratory → Brew + Drink
```lua
#showtooltip
/use [@player] Fermented Brew
```
> [!tip] Why it's useful
> The custom **Fermenter** recipe produces drinks that restore mana faster than standard water (custom value). Same pattern works for **Alchemy Laboratory** elixirs — put the custom consumable on one key and always have your buff up.

### Custom Potion Buff Check (Alchemy Lab)
```lua
#showtooltip
/cast [mod:shift] Elixir of Major Mageblood; Elixir of Fortitude
```
> [!tip] Why it's useful
> Custom-lab elixirs stack with normal ones on Forever. One key applies your lab elixir; Shift applies a second. Two buffs, one button, zero bag juggling.

---

## ⚒️ Legacy: Resourcefulness Tree

### Reinforce → Gear Repair Macro
```lua
#showtooltip
/run RepairAllItems()
```
> [!tip] Why it's useful
> **Reinforce** reduces repair costs. This script repairs everything at any vendor-repair NPC with one click — combine with a `/target` on the repair NPC if you want a full one-press "repair and go". *(RepairAllItems is client-side; works on WotLK-era UI.)*

### Diplomat → Rep Token Burn
```lua
#showtooltip
/use [mod:shift] Insignia of the Alliance
/use [nomod] Insignia of the Horde
```
> [!tip] Why it's useful
> **Diplomat** boosts rep gains. Forever has custom rep tokens (Darkspear care packages etc.). This burns your stored rep item in one keypress — plain for Horde, Shift for Alliance — so rep grinds don't eat your action bars.

---

## 🕳️ Custom Items: Lich's Index Finger & Friends

### Lich's Index Finger → Offensive Use
```lua
#showtooltip
/cast [@mouseover,harm,nodead][] Lich's Index Finger
```
> [!tip] Why it's useful
> Custom quest reward items like **Lich's Index Finger** are essentially free abilities. Putting them on a mouseover-harm macro means they hit exactly who you're hovering — no retargeting mid-combat.

### Custom Trinket Stack (all on-use items)
```lua
#showtooltip
/use 13
/use 14
/use [combat] Lich's Index Finger
```
> [!tip] Why it's useful
> Forever's custom on-use items (trinkets, quest rewards) all share the same "press to activate" pattern. Stacking them in one macro means your full custom-item burst fires on a single keypress during a fight.

---

## 🐾 Leveling Grind Kit (server-specific QoL)

### Skinning After Kill (Skinning + loot)
```lua
#showtooltip
/run if IsFishingLootable() then ... end
/interact
```
> [!tip] Why it's useful
> The leveling guide's #1 combo is **Skinning + Herbalism**. This interact script (WotLK-era: `/interact`) targets and skins the corpse you're looking at. With auto-loot on, it's one press per corpse — keeps the gold flowing between pulls.

### Herbalism Gather (mouseover node)
```lua
#showtooltip
/target [@mouseover,exists]
/interact
```
> [!tip] Why it's useful
> Hover a herb node and press — no clicking the tiny node hitbox. The guide says "pick everything," and this makes picking instant. *(WotLK-era `/interact` requires the target be an object you can interact with.)*

### Flight Path + Mount Priority (Frequent Flier)
```lua
#showtooltip
/cast [nocombat] Summon Random Favorite Mount
```
> [!tip] Why it's useful
> **Frequent Flier** unlocks flight paths early. This macro just mounts up — combine with a `#showtooltip` on a flight-master dialog if you want to fly the moment you dismount.

---

## 📋 Quick Reference

| Legacy Perk | Macro | Why |
|---|---|---|
| Field Medicine | Bandage self / Cure+bandage | Cheapest emergency heal |
| Field Guide | Quest item @cursor | One-click quest item use |
| Master Chef | Eat / Drink (mod) | No bag hunting while grinding |
| Bountiful Harvest | Cook → eat loop | Auto-craft + consume |
| Reinforce | RepairAllItems | One-click repair |
| Diplomat | Rep token burn | One-key rep grind |
| Custom recipes | Item use macros | Custom items = free abilities |
| Skinning/Herbalism | /interact macros | Instant gather per corpse/node |

---

> [!warning] Name checks
> Forever's custom recipes and items may have exact names that differ from examples here — hover the item in your bags and use the exact tooltip name. The **pattern** is what matters: `/use [condition] ExactItemName`.