# 🐉 World of Warcraft 3.3.5a (Wrath of the Lich King) Macro Collection

A curated collection of useful macros for **World of Warcraft: Wrath of the Lich King (3.3.5a)**.

Compatible with:

- Blizzard WotLK 3.3.5a
- Warmane
- AzerothCore
- TrinityCore
- ChromieCraft
- Most 3.3.5a private servers

---

# Table of Contents

- Getting Started
- Macro Basics
- Universal Macros
- Smart Mount Macros
- Mouseover Macros
- Focus Macros
- Arena & PvP
- Targeting
- Raid Utility
- Pet Macros
- Equipment Macros
- Castsequence
- Modifier Keys
- Consumables
- Engineering
- Party & Raid
- Useful Slash Commands
- Macro Conditionals
- Recommended Addons

---

# Getting Started

Open the Macro window by typing:

```
/macro
```

or

```
/m
```

You can create:

- Character-specific macros
- General account macros

Choose the **?** icon so the icon automatically changes depending on the spell currently being used.

---

# Macro Basics

Every macro should usually begin with:

```lua
#showtooltip
```

This automatically displays:

- Spell icon
- Item icon
- Cooldown
- Tooltip

---

# Universal Macros

## Start Attack

```lua
#showtooltip Sinister Strike
/startattack
/cast Sinister Strike
```

---

## Stop Attack

```lua
/stopattack
```

Useful before:

- Sap
- Polymorph
- Repentance
- Freezing Trap

---

## Stop Casting

```lua
#showtooltip Counterspell
/stopcasting
/cast Counterspell
```

Perfect for:

- Counterspell
- Kick
- Pummel
- Wind Shear
- Mind Freeze

---

## Cancel Aura

```lua
/cancelaura Ice Block
```

Examples:

```lua
/cancelaura Hand of Protection
```

```lua
/cancelaura Divine Shield
```

---

# Smart Mount Macros

## Automatic Ground / Flying / Swimming Mount

Automatically chooses the correct mount depending on where your character is.

```lua
#showtooltip
/dismount [mounted]
/cast [swimming] Sea Turtle
/cast [flyable] Blue Drake
/cast Black War Tiger
```

### How it works

| Condition | Mount |
|-----------|------|
| Swimming | Sea Turtle |
| Flying allowed | Blue Drake |
| Otherwise | Black War Tiger |

---

## Random Mounts

```lua
#showtooltip
/dismount [mounted]
/cast [swimming] Sea Turtle
/userandom [flyable] Blue Drake, Bronze Drake, Red Drake
/userandom Black War Tiger, Black War Bear, Swift White Hawk
```

---

## Modifier Mounts

```lua
#showtooltip
/dismount [mounted]
/cast [mod:shift] Traveler's Tundra Mammoth
/cast [mod:ctrl] Sea Turtle
/cast [flyable] Blue Drake
/cast Black War Tiger
```

| Key | Mount |
|------|------|
| Shift | Mammoth |
| Ctrl | Sea Turtle |
| Default | Smart Mount |

---

# Mouseover Macros

## Heal Mouseover

```lua
#showtooltip Flash Heal
/cast [@mouseover,help,nodead][] Flash Heal
```

---

## Dispel Mouseover

```lua
#showtooltip Cleanse
/cast [@mouseover,help,nodead][] Cleanse
```

---

## Resurrection Mouseover

```lua
#showtooltip Resurrection
/cast [@mouseover,help,dead][] Resurrection
```

---

# Focus Macros

## Set Focus

```lua
/focus
```

---

## Clear Focus

```lua
/clearfocus
```

---

## Focus Crowd Control

```lua
#showtooltip Polymorph
/cast [@focus] Polymorph
```

---

## Focus Interrupt

```lua
#showtooltip Counterspell
/stopcasting
/cast [@focus] Counterspell
```

---

## Focus Blind

```lua
#showtooltip Blind
/cast [@focus] Blind
```

---

# Arena & PvP

## PvP Trinket

Top Trinket

```lua
/use 13
```

Bottom Trinket

```lua
/use 14
```

---

## Burst Macro

```lua
#showtooltip
/use 13
/cast Avenging Wrath
```

---

## Shadowstep Kick

```lua
#showtooltip Kick
/cast Shadowstep
/cast Kick
```

---

## Focus Sap

```lua
#showtooltip Sap
/cast [@focus] Sap
```

---

# Targeting

## Target Last Target

```lua
/targetlasttarget
```

---

## Assist Tank

```lua
/assist TankName
```

---

## Target Arena Players

```lua
/target arena1
```

```
arena2
arena3
arena4
arena5
```

---

# Raid Utility

## Ready Check

```lua
/readycheck
```

---

## Raid Warning

```lua
/rw Stack on Boss!
```

---

## DBM Pull Timer

```lua
/dbm pull 10
```

---

# Pet Macros

## Attack

```lua
/petattack
```

---

## Follow

```lua
/petfollow
```

---

## Passive

```lua
/petpassive
```

---

## Stay

```lua
/petstay
```

---

## Defensive

```lua
/petdefensive
```

---

# Equipment Macros

## Equip Weapon

```lua
/equip Shadowmourne
```

---

## Equip Shield

```lua
/equip Bulwark of Azzinoth
```

---

## Fishing

```lua
#showtooltip Fishing
/equip Mastercraft Kalu'ak Fishing Pole
/cast Fishing
```

---

# Castsequence

## Basic Rotation

```lua
#showtooltip
/castsequence reset=target Corruption, Curse of Agony, Immolate
```

---

## Reset after Combat

```lua
/castsequence reset=combat Spell1, Spell2
```

---

## Reset after Time

```lua
/castsequence reset=5 Frostbolt, Ice Lance
```

---

# Modifier Keys

## Shift

```lua
#showtooltip
/cast [mod:shift] Frost Nova
/cast Frostbolt
```

---

## Ctrl

```lua
#showtooltip
/cast [mod:ctrl] Cone of Cold
/cast Frostbolt
```

---

## Alt

```lua
#showtooltip
/cast [mod:alt] Ice Lance
/cast Frostbolt
```

---

# Self Cast

```lua
#showtooltip
/cast [@player] Power Word: Shield
```

---

# Friendly / Enemy Macro

```lua
#showtooltip
/cast [help] Flash Heal; Smite
```

Friendly target:

- Flash Heal

Enemy target:

- Smite

---

# Party Healing

```lua
/cast [@party1] Flash Heal
```

```lua
/cast [@party2] Flash Heal
```

```lua
/cast [@party3] Flash Heal
```

```lua
/cast [@party4] Flash Heal
```

---

# Consumables

## Healthstone

```lua
/use Healthstone
```

---

## Healing Potion

```lua
/use Runic Healing Potion
```

---

## Mana Potion

```lua
/use Runic Mana Potion
```

---

# Engineering

## Nitro Boosts

```lua
/use Nitro Boosts
```

---

## Saronite Bomb

```lua
/use Saronite Bomb
```

---

## Frag Belt

```lua
/use Frag Belt
```

---

# Useful Slash Commands

```
/macro
/m
/reload
/camp
/logout
/startattack
/stopattack
/focus
/clearfocus
/petattack
/petfollow
/petstay
/petpassive
/use
/equip
/script
/run
/cancelaura
/readycheck
```

---

# Macro Conditionals

| Conditional | Description |
|------------|-------------|
| `[help]` | Friendly target |
| `[harm]` | Enemy target |
| `[exists]` | Target exists |
| `[dead]` | Dead target |
| `[nodead]` | Living target |
| `[combat]` | In combat |
| `[nocombat]` | Out of combat |
| `[mounted]` | Mounted |
| `[nomounted]` | Not mounted |
| `[flyable]` | Flying allowed |
| `[swimming]` | Swimming |
| `[stealth]` | In stealth |
| `[mod:shift]` | Shift key |
| `[mod:ctrl]` | Ctrl key |
| `[mod:alt]` | Alt key |
| `[@player]` | Yourself |
| `[@mouseover]` | Mouseover target |
| `[@focus]` | Focus target |

---

# Recommended Addons

## PvE

- Deadly Boss Mods
- Quartz
- OmniCC
- WeakAuras
- Bartender4

## PvP

- Gladius
- LoseControl
- OmniCC
- Quartz

## Healers

- Clique
- Grid2
- HealBot

---

# Notes

- Macros **cannot automate gameplay**.
- Only **one global cooldown (GCD)** ability can be activated per key press.
- `#showtooltip` should be used whenever possible.
- Mouseover and Focus macros are essential for healing and PvP.
- Smart mount macros save action bar space and automatically select the correct mount based on your environment.

---

## ⭐ Contributing

Pull requests are welcome!

If you have useful class macros, PvP tricks, profession macros, or quality-of-life improvements, feel free to contribute and help expand this collection for the entire WotLK community.
