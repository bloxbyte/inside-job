# 🌟 INSIDE JOB - Game Design Document (Revised)

## Overview

**Genre:** Co-op Heist / Strategy / Espionage-Action
**Player Count:** 1–4 players per lobby
**Core Loop:** Plan ➜ Infiltrate ➜ Extract ➜ Upgrade

---

## 🏠 The Bunker (Hub)

**Setting:** Converted underground operations center blending hacker den and logistics HQ.
**Interactive Areas:**

* **Ops Board:** Accept contracts from corporate fixers and underground brokers.
* **Forge:** Craft disguises, gadgets, and forged credentials.
* **Vault:** Store stolen data chips, artifacts, and blueprints.
* **Comms Bay:** Manage contacts and track faction reputation.
* **Vehicle Lift:** Deploy via covert transport, drone carrier, or disguised van.

**Technical Notes:**

* Max 4 players per instance.
* `TeleportService` connects the hub to mission environments.
* `DataStoreService` stores player XP, intel credits, and unlocks.

---

## 🎬 Phase 1: Operation Setup

**Flow:**

1. Crew gathers around the holographic planning table.
2. 3D site projection displays mission details (target, security level, and objectives).
3. Players vote on **approach type**: *Silent Entry*, *Social Engineering*, or *Forceful Extraction*.
4. Optional **insider contacts** can be bribed to reveal shortcuts or disable systems.

**Updated Roles:**

| Role        | Abilities                                   | Signature Tools               |
| ----------- | ------------------------------------------- | ----------------------------- |
| Infiltrator | Stealth, disguise, temporary staff access   | Voice modulator, lockpick     |
| Technician  | Hacking, disables drones & security         | EMP drone, hacking pad        |
| Field Agent | Combat support, heavy lifting               | Stun rifle, reinforced gloves |
| Coordinator | Crew buffs, marks targets, calls extraction | Smart tablet, drone beacon    |

**Extras:**

* Animated holographic briefings.
* Gear loadout screen prior to deployment.

---

## 🔥 Phase 2: Infiltration & Execution

**Example Mission: Data Center Breach**

* **Zones:** Reception, Server Core, R&D Vault, Rooftop Extraction.
* Dynamic systems: biometric locks, camera grids, and autonomous patrol drones.

**Core Mechanics:**

* **Threat Level Meter** — measures suspicion buildup instead of noise.
* **Fake IDs & Credentials** — allow players to blend in until scanned or spotted.
* **Power rerouting & access puzzles** — environmental mini-events to advance progress.
* Security forces adapt dynamically based on detection history.

**Player States:**

* Normal, Compromised, Extracting.
* Teammates can reset suspicion by triggering diversions.

---

## 🚨 Phase 3: Extraction

**Flow:**

* Extraction may require holding an upload zone or transporting physical prototypes.
* Escape options vary: **cargo elevator**, **drone pickup**, or **maintenance tunnel**.
* Side objectives appear dynamically during high alert.

**Outcome:**

* Clean Extraction = Full Intel Bonus.
* Alerted Escape = Reduced Reputation Gain.

---

## 💼 Phase 4: Payout & Progression

**End Screen:**

* Intel Credits, Reputation, and Performance Rank summary.
* Clean run bonuses, stealth streak multipliers, and faction reputation updates.

**Unlocks:**

| Level | Unlock                      |
| ----- | --------------------------- |
| 2     | Noise-cancelling boots      |
| 5     | Advanced stealth drone      |
| 10    | Deepfake mask system        |
| 15    | Hidden comms room upgrade   |
| 20    | Faction-exclusive contracts |

**Hub Customization:**
Decor, lighting presets, digital trophy wall, and interactive mission replays.

---

## 🧠 Tech Design

**Core Modules:**

| Module           | Description                                               |
| ---------------- | --------------------------------------------------------- |
| MissionManager   | Handles operation flow, triggers, and adaptive objectives |
| RoleSystem       | Role abilities, XP scaling, loadout logic                 |
| SecurityAI       | Adaptive guards, drones, and patrol heuristics            |
| IntelSystem      | Tracks stolen data, rewards, and reputation               |
| ThreatSystem     | Global suspicion & alert control                          |
| ExtractionSystem | Handles escape routes and phase transitions               |
| DataStoreService | Persistent player and crew data                           |

---

## 🎨 UI & Visual Style

**Briefing UI:** Minimal holographic aesthetic with cool cyan highlights.
**HUD:** Threat level bar (top right), Objective tracker (bottom left), Crew signal panel.
**End Screen:** Intel analysis animation and smooth cinematic transitions.

---

## ⚙️ Expansions & Events

* **Double Agent Update:** Missions where one player has hidden objectives.
* **Prototype Heist:** Steal unstable experimental tech before security lockdown.
* **Data Leak Season:** Timed events altering faction dynamics and contract types.
* **Hardline Mode:** Permanent death for the run; increased rewards.

---

## 💸 Monetization (Non-P2W)

* **Cosmetics:** Tactical suits, masks, and data-visor effects.
* **Hub Decor:** Lighting kits, hologram tables, and trophies.
* **Drone & Vehicle Skins:** Stealth, corporate, or elite themes.
* **Season Pass:** New operations, story arcs, and exclusive visual gear.

---

## 🚀 Development Roadmap (Summary)

**Phase 1 (Prototype)**

* Core infiltration and extraction mechanics.
* Basic AI and alarm systems.

**Phase 2 (Core Systems)**

* Role abilities, threat management, and dynamic AI.
* Data & intel-based progression.

**Phase 3 (Visuals + UI)**

* Holographic planning room, stealth HUD, and interactive briefings.

**Phase 4 (Beta Launch)**

* Player progression, persistent hub, and early contracts.

**Phase 5 (Full Release)**

* Expanded heist roster, faction system, and seasonal events.
