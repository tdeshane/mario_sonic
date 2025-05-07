# Mario vs Sonic Mega Battlefield Edition

## Overview
Players begin by selecting one of four modes: Duel, Battle Royal, Global Battle Royal, or World Orb Mode. After character selection, a stage is randomly chosen. Matches last up to 5 minutes or until one side is eliminated. Players deplete opponents’ HP cubes or knock them out of bounds to score eliminations. At match end, participants earn coins, experience, and badges based on damage, wins, and style. Progression unlocks new fighters, weapons, power-ups, and hidden boards.

### Game Loop
- **Character & Loadout**: Pick fighter and up to two weapon/power-up slots.
- **Stage Initialization**: Random board with dynamic hazards.
- **Battle Phase**: Combat using combos, weapons, abilities, and environment.
- **Conclusion**: Score tallied; rewards distributed; achievements tracked.
- **Progression**: Unlock content via badges, currency, and milestone rewards.

## Battle Boards
### Prototype Boards (10/100+)
1. **Bowser's Castle**
   - **Layout**: Three-tier platforms arranged around central lava moat; side walkways for flank attacks.
   - **Hazards**:
     - Lava cubes rise every 20s, reducing ground space.
     - Flame traps shoot blasts from floor cubes on 2s warning.
     - Rotating platform shifts position every 15s.
   - **Items**: Weapon crates spawn at center every 30s.

2. **Greenfield**
   - **Layout**: Open grass cube field with gentle hills and two small mushroom platforms.
   - **Hazards**:
     - Breakable crate cubes drop from above; may contain items or harm players.
     - Roaming Goomba cubes patrol fixed paths, acting as moving obstacles or platforms.
   - **Items**: Random drops from roaming Goombas.

3. **Robotic Hazmen**
   - **Layout**: Industrial cube factory with multiple conveyor belts and catwalks.
   - **Hazards**:
     - Laser turrets fire beams across lanes at 10s intervals.
     - Electrified floor cubes toggle on/off every 5s.
     - Conveyor belts carry players toward crusher arms.

4. **Aquadic Surf**
   - **Layout**: Water cube arena with floating platforms and central tube slide.
   - **Hazards**:
     - Water cubes slow movement by 50%.
     - Periodic water-jet hazards push players off platforms.
     - Rising flood cubes submerge lower platforms after 30s.

5. **Sky Top Cruise**
   - **Layout**: Floating island cubes connected by narrow bridges.
   - **Hazards**:
     - Wind gust voxels blow players along set paths.
     - Collapsing bridge cubes fall away after 5s of use.
     - Random lightning strikes on designated cubes.

6. **Super Smash Mayhem**
   - **Layout**: Central stage with rotating platforms and outer zones.
   - **Hazards**:
     - Random hazard cubes: spikes, springs, acid pools.
     - Platforms rotate direction and speed every 10s.

7. **Wreak Site**
   - **Layout**: Construction zone with scaffolding and debris fields.
   - **Hazards**:
     - Explosive barrel cubes detonate on impact.
     - Crushing robot arms sweep across lanes.
     - Shrapnel cubes spawn near wreckage.

8. **Alexia's Dungeon of Death**
   - **Layout**: Maze-like dark cube corridors leading to an arena.
   - **Hazards**:
     - Spike trap cubes emerge from floor on pressure.
     - Skeleton warrior cubes patrol chambers.
     - Poison gas cubes fill rooms in waves.

9. **Mount Fuji**
   - **Layout**: Sloped ice cubes with narrow ridges and summit platform.
   - **Hazards**:
     - Slippery ice cubes reduce traction.
     - Avalanche cubes tumble down slopes every 20s.
     - Frost cubes slow attack speed in cold zones.

10. **Slime Swamp Factory**
   - **Layout**: Flooded factory floor with slime pits and pumps.
   - **Hazards**:
     - Sticky slime cubes trap players for 3s.
     - Acid spray traps emit from pipes on 8s cooldown.
     - Conveyor slime belts move players toward hazard zones.

- …and 90+ additional boards (e.g., Cyber City Ruins, Volcanic Pit, Ancient Temple).

## Weapons & Abilities
### Weapon Stats Table
| Weapon      | Damage | Range | Cooldown | Effect                      |
| ----------- | ------ | ----- | -------- | --------------------------- |
| Hammer      | 25     | Melee | 1s       | Stun 0.5s                   |
| Robot Clone | —      | 8m    | 12s      | Summons AI ally to fight    |
| Fire Bomb   | 40     | 10m   | 5s       | 3m radius burn damage       |
| Nuke        | 100    | 15m   | 30s      | Massive AoE, destroys cubes |
| Gravity Gun | —      | 12m   | 8s       | Pulls enemies toward user   |
| Tri Laser   | 30×3   | 20m   | 4s       | Fires 3 beams in spread     |
| Vacuum      | —      | 6m    | 6s       | Draws items and small cubes |
| Ghost Box   | —      | Self  | 12s      | Grants 3s invincibility     |
| …hundreds more defined similarly                                                    |

### Move System
- **Light Combo**: 3-hit sequence.
- **Heavy Attack**: Knockback effect.
- **Special Ability**: Unique to each fighter.
- **Aerial Move**: High mobility in air.
- **Ultimate Move**: Charges via damage; unleashes signature finisher.

##### Sample Moves
- **Mario**: Fireball (Special), FLUDD Boost (Aerial), Super Ground Pound (Ultimate).
- **Sonic**: Spin Dash (Special), Homing Attack (Light Combo), Super Speed Rush (Ultimate).
- **Alexia**: EMP Blast (Special), Robo-Charge (Heavy), Galaxia Storm (Ultimate).

## Fighters
| Fighter             | Tier    | Unlock Condition                                   |
| ------------------- | ------- | -------------------------------------------------- |
| Mario               | Starter | —                                                  |
| Luigi               | Starter | —                                                  |
| Peach               | Starter | —                                                  |
| Daisy               | A       | Win 10 Duels                                       |
| Sonic               | Starter | —                                                  |
| Shadow              | B       | Global Event Completion                           |
| Dr. Robotnik        | B       | Defeat in Robotic Hazmen                           |
| Kirby               | A       | Slay 100 enemies                                   |
| Captain Falcon      | B       | Time Trial: <2 min                                 |
| Polio               | C       | Hidden spawn                                       |
| Baby Hamster        | C       | Easter Egg Quest                                   |
| Chicken Jockey      | C       | Easter Egg Quest                                   |
| Steve               | S       | Minecraft Crossover Event                          |
| Ender Dragon        | S       | End Arena Boss                                    |
| Bunrth (Giant Boar) | A       | Wreak Site Boss Fight                              |
| Alexia              | S       | Found/Defeated in Alexia's Dungeon of Death        |
| Piccachu            | B       | Trade Special Event                                |
| Charizard           | B       | Pokémon Event                                      |
| Rose                | B       | Slime Swamp Factory Hidden Quest                   |
| Peke (Pink Mouse)   | C       | Royal Battle Reward                                |
| Princutia           | A       | Peace Negotiation Side Quest                       |
| …more hidden fighters                                                              |

## Progression & Economy
### Currencies
- **Coins**: +1 per 10 damage dealt.
- **Gold**: +10 per victory.
- **Diamonds**: Rare (milestone rewards).
- **Badges**: Awards for achievements (board completion, master moves).

### Upgrades & Power-Ups
- Weapon upgrades: damage↑, cooldown↓.
- Skins: cosmetic only.
- In-game power-ups: Speed Boost, Shield Cube, Damage Amp.

## Legendary Challenges
### The Guffin
- Appearance: Bird head + lion body cube monster.
- Unlock: Collect 5 Ancient Keys across boards.
- Fight: 3-phase boss with cube transformations.

## Hidden Content
### Alexia’s Dungeon
- 3 chambers with puzzles, spike traps, skeleton cubes.
- Final boss: Alexia with AI-driven tactics.

## Game Modes
- **Duel**: 2 players, best of 3.
- **Battle Royal**: 16 players, last player standing.
- **Global Battle Royal**: 18+ worldwide, 30-min limit.
- **World Orb Mode**: Team smash Orb 3× to win.

## Multiplayer & Trading
- Regional matchmaking (4 regions).
- Global lobbies for 18+ events.
- Monster trading: 1:1 equal power trades.
- Seasonal Magic vs Power events.

## Next Steps
1. Board Level Design & Cube Hazard Prototypes
2. Weapon Balance & Prototype Moves
3. Fighter Animation Rigs & Move Implementation
4. Network Architecture & Lobby UI
5. Progression System & Economy Balancing
6. Hidden Dungeon & Boss AI
7. UI/UX Flow for Menus & Matchmaking

---
**PR Breakdown**
- **PR 2 – Weapon & Abilities System**
  - Weapon stats table & base classes
  - Core weapon scripts & prefabs
  - Power-up integration
- **PR 3 – Character Move System & Roster**
  - Move set framework & combo logic
  - Character controller enhancements
  - Unlock condition implementation
- **PR 4 – Board Environments & Hazards**
  - Level templates & cube asset library
  - Environmental hazard triggers
  - 10 prototype boards populated
- **PR 5 – Progression & Economy**
  - Currency systems & reward calculations
  - Achievement & badge modules
  - Upgrade & power-up mechanics
- **PR 6 – Multiplayer & Trading**
  - Networking foundation & matchmaker
  - Trade system UI & server auth
  - Regional vs global logic
- **PR 7 – Hidden Content & Boss AI**
  - Dungeon layouts & trap scripts
  - Guffin & Alexia boss phase AI
- **PR 8 – UI/UX & Polish**
  - Main menu & HUD
  - Balance tweaks & bug fixes
