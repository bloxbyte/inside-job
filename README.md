# 🌟 INSIDE JOB - Game Design Document

## Overview
**Genre:** Co-op Heist / Strategy / Stealth-Action  
**Player Count:** 1–4 players per lobby  
**Core Loop:** Plan ➜ Execute ➜ Escape ➜ Upgrade

---

## 🏠 Hideout / Hub

**Setting:** Underground warehouse or modern loft base.  
**Interactive Areas:**  
- **Gear Bench:** Buy & equip items.  
- **Mask Wall:** Customize masks.  
- **Crew Terminal:** Invite friends & form teams.  
- **Vehicle Bay:** Choose and upgrade escape vehicles.  

**Technical Notes:**  
- Max 4 players per server.  
- Use `TeleportService` to move players from hub to heist instances.  
- Data stored via `DataStoreService` (XP, cash, gear, cosmetics).

---

## 🎬 Phase 1: Planning

**Flow:**  
1. Players gather around planning table.  
2. UI lists jobs (Bank, Casino, Jewelry Store, etc.).  
3. Each job shows target, payout range, and difficulty.  
4. Players choose **roles**:

| Role | Abilities | Tools |
|------|------------|-------|
| Hacker | Disable cameras, hack vaults | Laptop, EMP |
| Enforcer | Carry heavy bags, break doors | Crowbar, shotgun |
| Infiltrator | Move silently, disguise | Lockpick, fake ID |
| Driver | Handles vehicle escape | Keycard, smoke grenades |

**Extras:**  
- Mission briefing cinematic.  
- Loadout selection before deployment.

---

## 🔥 Phase 2: Heist Execution

**Example Map: Bank Heist**  
- **Zones:** Lobby, Offices, Vault Corridor, Vault Room, Escape Alley.  
- Dynamic systems: guard patrols, security cameras, NPC civilians.

**Core Mechanics:**  
- Noise Meter — triggers guards if too high.  
- Vision Cones — guards detect players.  
- Hacker can disable alarms for 30 seconds.  

**Player States:**  
- Normal, Detained, Escaped.  
- Teammates can rescue detained players.  

---

## 🚗 Phase 3: Getaway

**Flow:**  
- Driver pings escape route on minimap.  
- Police waves spawn dynamically.  
- Players reach escape zone to win.  
- Failure = reduced payout.  

**Escape Types:**  
- Car chase  
- Boat (coastal map)  
- Helicopter (elite mission)

---

## 💰 Phase 4: Payout & Upgrades

**End Screen:**  
- Cash & XP summary.  
- Stealth bonuses.  
- Crew reputation update.

**Unlocks:**  
| Level | Unlock |
|--------|--------|
| 2 | Silenced pistol |
| 5 | Armored vehicle |
| 10 | Casino Heist |
| 15 | Mask editor |
| 20 | Crew logo creator |

**Hideout Customization:**  
Furniture, lighting themes, trophies.

---

## 🧠 Tech Design

**Core Modules:**  
| Module | Description |
|---------|--------------|
| MissionManager | Handles heist flow & triggers |
| RoleSystem | Abilities & loadouts per role |
| NPCSystem | Guard AI & patrols |
| LootSystem | Loot bags, payout values |
| AlarmSystem | Global alert handling |
| VehicleSystem | Escape routes & car logic |
| DataStoreService | Persistent saves |

---

## 🎨 UI & Visual Style

**Planning UI:** Dark interface with red highlights, looping video backgrounds.  
**HUD:** Noise bar (top right), Objective tracker (bottom left), Crew status icons.  
**End Screen:** Money counting animation, cinematic transitions.

---

## ⚙️ Expansions & Events
- **Undercover Ops:** Infiltrate disguised as guards.  
- **Night Market Job:** Steal from shipment hub.  
- **Black Market Update:** Craftable gear & gadgets.  
- **Hardcore Mode:** No respawns, higher rewards.

---

## 💸 Monetization (Non-P2W)
- **Cosmetics:** Unique masks & outfits.  
- **Hideout Decor:** Theme packs.  
- **Vehicle Skins:** Tactical or luxury.  
- **Season Pass:** New heists & limited cosmetics.

---

## 🚀 Development Roadmap (Summary)

**Phase 1 (Prototype)**  
- Basic heist flow (enter, loot, escape).  
- Simple NPC AI & loot interaction.  

**Phase 2 (Core Systems)**  
- Role system & stealth mechanics.  
- Alarm / police response logic.  

**Phase 3 (Visuals + UI)**  
- Planning room, heist HUD, end screen polish.  

**Phase 4 (Beta Launch)**  
- Add progression, save data, monetization.  

**Phase 5 (Full Release)**  
- Multiple heists, crew leaderboards, expansions.