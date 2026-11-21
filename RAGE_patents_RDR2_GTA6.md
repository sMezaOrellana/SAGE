# Patents covering RAGE systems (focus: RDR2 & GTA VI)

Compiled 2026-11-20. Data comes from individual Google Patents pages (`https://patents.google.com/patent/<NUMBER>/en`), checked one by one. Inventors were placed at a studio using MobyGames credits, in-game credits (gta.wiki), Rockstar's official GTA VI credits, GDC talks and press.

## How to read this

- **No patent names RAGE, GTA or Red Dead.** Every Rockstar patent is filed in the name of **Take-Two Interactive Software, Inc.** No Rockstar company appears as assignee on any patent. A patent counts as "RAGE" here when its inventors are Rockstar engineers working on RAGE subsystems at the time it was filed.
- **A patent doesn't prove the tech shipped in a game.** Links to RDR2 or GTA VI come from inventor credits and timing, not from the patents themselves.
- **"Rockstar" assignee searches pull in an unrelated company.** Rockstar Consortium / Rockstar Bidco holds Nortel's old patents. It is excluded.
- **Coverage.** I found 43 US grants from Take-Two's own filings through 2025, which matches the count from Patent Leaderboard, a third-party site. The blind spot is new publications: US applications are published about 18 months after filing, so GTA VI-era filings from 2025–26 may not be public yet.

---

## 1. Rockstar-invented, RDR2 / GTA VI era (priority 2017+). All active.

### AI / navigation
| Patent(s) | Title | Priority | Granted | Inventors (Rockstar role) | What it covers |
|---|---|---|---|---|---|
| **US11071916B2**, **US11684855B2** (pubs US20200338450A1, US20210316220A1) | System and method for virtual navigation in a gaming environment | 2019-04-24 | 2021-07-27; 2023-06-27 | Simon Parr (Rockstar North lead AI programmer; RDR2 vehicle/traffic AI; GTA VI AI/Gameplay Tech), David Hynd (Rockstar North VP Technology; GTA VI) | Pathfinding over a coarse graph built from low-level road-network nodes (traffic, pursuit routing) |

### Animation
| Patent(s) | Title | Priority | Granted | Inventors (Rockstar role) | What it covers |
|---|---|---|---|---|---|
| **US11620781B1** | System and method for virtual character locomotion | 2019-10-25 | 2023-04-04 | Tobias Kleanthous (RDR2 locomotion & player-control programmer; gave the GDC 2021 talk on RDR2's horses), Mike Jones (animation director), Chris Swinhoe (TD AI/Gameplay), Arran Cartie (lead gameplay animator), James Stuart Miller (VP Tech R&D, animation), Sven van Soom (lead animation-systems programmer) | Data-driven animation "building blocks" (motion, motion-type and archetype blocks plus a blackboard) defined separately from core engine code |
| **US11951384B2** (pub US20220134218A1) | System and method for virtual character animation using motion capture | 2020-11-02 | 2024-04-09 | James Stuart Miller, Gustavo Eggert Boehs (Rockstar Toronto ML R&D; says he spent 6 yrs on GTA VI), Cory Alderman and Adam De Oliveira (motion-capture supervisors, RDR2) | Neural-network hand-pose prediction from optical markers plus glove sensors |
| **US20250095261A1** (app 18/885,149), **pending** | System and method for runtime retargeting | 2023-09-15 | none yet (a non-final office action, i.e. an examiner's first rejection, was reportedly issued Mar 2026) | Eray Molla, Peter Sandilands (animation programmers credited on RDR2), James Stuart Miller, Mark Tennant (Rockstar North animation director), Ahmad Abdul Karim, Frank David Kozuh, Colin John Graham | Adapting pre-authored ("fixed-source") motion in real time to whatever the character runs into during play |

### Rendering
| Patent(s) | Title | Priority | Granted | Inventors (Rockstar role) | What it covers |
|---|---|---|---|---|---|
| **US11534688B2**, **US12263404B2** (pubs US20190299097A1, US20230141387A1) | Method and apparatus for enhanced graphics rendering in a video game environment | 2018-04-02 | 2022-12-27; 2025-04-01 | Alex Hadjadj (RDR2 TD Graphics & VFX; GTA VI VP Graphics Tech), Raymond Kerr, Steve Reed, Tyler Robertson (Rockstar San Diego graphics), Owen Shepherd (RDR2 lighting director), Flavius Alecu, Rick Stirling (technical art) | Global illumination: reflected light stored in a per-texel RGB map, height derived from depth, bounced light computed per pixel. Filed ~6 months before RDR2 shipped |

### World / asset construction
| Patent(s) | Title | Priority | Granted | Inventors (Rockstar role) | What it covers |
|---|---|---|---|---|---|
| **US10427046B2**, **US10987587B2** (pubs US20190192970A1, US20190192972A1) | System and method for game object and environment generation | 2017-12-22 | 2019-10-01; 2021-04-27 | Aaron Garbut (Rockstar North art director), Klaas Schilstra (assoc. technical director), Flavius Alecu, John Whyte (RDR2 lead engine programmer) | Building and rendering in-game objects from metadata records (asset IDs plus property tags) |

### Online: Red Dead Online / GTA Online
| Patent(s) | Title | Priority | Granted | Inventors (Rockstar role) | What it covers |
|---|---|---|---|---|---|
| **US10814233B2**, **US11192032B2**, **US11794114B2** | System and method for session management in a multiplayer network gaming environment | 2017-11-08 | 2020-10-27; 2021-12-07; 2023-10-24 | Philip Degarmo, Robert Schmitz (Rockstar San Diego networking; RDR2 networking) | Merging and splitting network sessions seamlessly as players move through the world, with no loading screens |
| **US11027196B2**, **US11992755B2** | System and method for managing transactions in a multiplayer network gaming environment | 2019-09-04 | 2021-06-08; 2024-05-28 | Kevin Baca (Rockstar San Diego chief architect, online services), Chris Mueller (GTA VI platform services) | Dedicated game servers: remote-procedure-call (RPC) function sets, and access tokens issued after the server checks an authorization ticket |
| **US11273380B1** | Method and apparatus for preventing cheating … by providing obfuscated game variables | 2019-10-25 | 2022-03-15 | Kevin Feeney (VP InfoSec), Amir Soofi (GTA VI TD Security Tech), Martin Hedlund | Anti-cheat: each game variable is split into a descriptor plus a raw chunk, then transformed, sliced and masked across a memory pool |

## 2. Rockstar-invented, earlier RAGE online foundation (priority 2013, from the Max Payne 3 / GTA V / GTA Online era). All active, expiring roughly 2033–34.

The four 2013 families below were filed as sister applications on the same day. RAGE's later online stack, Red Dead Online included, builds on this layer.

| Patent(s) | Title | Inventors | What it covers |
|---|---|---|---|
| **US9805067B1**, **US9977795B1** | System and method for multiplayer network gaming | Ian Cottrell (assignment chain runs through Rockstar London Ltd) | Peer-to-peer multiplayer driven by scripted high-level events, with host migration |
| **US10195520B1** | System and method for network gaming architecture | Dan Conti (Social Club), Evan Michaels, Kevin Baca | Script files that change live game behaviour without a full patch |
| **US9814967B1** | System and method for time flow adjustment in multiplayer games | Jason Bone (credited as Max Payne 3 lead designer) | Slow-motion that applies only to the players in line of sight, i.e. multiplayer "bullet time" |
| **US9839838B1**, **US9901831B2** | System and method for online community management | Dan Conti, Evan Michaels, Pau Aguilar Fruto | Automatic plus peer-reported bad-sportsmanship and cheater detection (the "Bad Sport" concept) |

## 3. Middleware inside RAGE that Take-Two now owns

**NaturalMotion** makes euphoria, used in GTA IV, RDR, GTA V and RDR2. Take-Two has controlled it directly since 2022-05-23. The patents remain in NaturalMotion's name, and Take-Two keeps paying the US maintenance fees.

| Patent | Title | Status | RAGE relevance |
|---|---|---|---|
| US7685081B2 / EP1392556B1 (Torsten Reil, 2001) | Bipedal walking simulation / neural motion controller | **Expired** (2022) | Core of euphoria/DMS (Dynamic Motion Synthesis, the tech euphoria is built on) |
| **US8730245B2** | Defining an animation of a virtual object within a virtual world | In force, ~2032 | morpheme animation graph with physics nodes |
| **US9449416B2** (Chapman, Lowe, 2012) | Animation processing of linked object parts | In force to 2033-08-05 (Google lists Zynga as assignee; the USPTO assignment record says NaturalMotion) | Closest to euphoria's design. A behaviour module drives limb groups using collision flags and a time factor based on how long the character takes to fall its own height, then sends a scaled target pose to a controller |
| **US8228336B1**, Lucasfilm (not Take-Two), 2008 | Integrating a motion synthesis system into a video game system | In force to ~2028-01-23 | The only patent found that names "the Euphoria system available from NaturalMotion". Claim 1: switch off collisions for character parts that are stuck inside each other, run motion synthesis plus physics for a set time, then switch collisions back on |
| US9652879B2, US9984488B2, US10062197B2, US10410393B2, US10297066B2 | Animating a virtual object (Aguado/Brewster, 2013–16) | In force (US10297066B2's 8th-year fee is due **2026-11-21**) | Mostly Zynga-era mobile IK work; loosely related |

No patent appears to claim euphoria's behaviour-driven active ragdoll itself. It looks like a trade secret.

## 4. Excluded: Take-Two patents that are *not* RAGE

These were invented by 2K / Visual Concepts or come from acquisitions. Several get passed around online as "GTA 6 patents" by mistake.

- **US11978162B2**, continuous LOD: NBA 2K engineers (Brooks, Best, Pepper, Krazanowski, Snyder). *Often misreported as GTA VI.*
- **US9922141B2 / US10685152B2**, sparse fluids ("sweat/blood/rain"): Matthias Wloka, 2K Sports, 2006. *Often misreported as GTA VI.*
- **US8941664B2 / US10395410B2**, pose-based deformation: Jason Dorie, NBA 2K, 2006. *Often misreported as GTA VI.*
- **US9855499B2 / US10503963B2**, player-likeness image capture: Tim Meekins (NBA 2K engineer). Most likely the NBA 2K face scan.
- **US8016664B2 family**, simulating a particular user: Visual Concepts, 2005.
- **Pre-2012 rendering patents (inventors not traced to a studio, not RAGE-era):**
  - ambient occlusion: US8390621B2, US8847958B2, US9251622B2
  - fluids visualization: US8237722B2
  - lights and shadows: US8368693B2, US9349214B2, US9928641B2
  - visual-object filtering: US9684975B2
  - music creator: US7884275B2
- **Yoom/Tetavi volumetric-video portfolio** (10 families, assigned to Take-Two 2025): not RAGE.
- **Mad Doc Software** (later Rockstar New England), speech-recognition app US20060040718A1: abandoned.
- **Angel Studios** (Rockstar San Diego's predecessor, origin of the RAGE codebase): no patents found.

## Sources
- Google Patents pages for every number above
- Rockstar GTA VI credits: https://www.rockstargames.com/VI/credits
- GTA Online credits by studio: https://gta.wiki/w/Grand_Theft_Auto_Online/Credits
- MobyGames RDR2 credits: https://www.mobygames.com/game/115902/red-dead-redemption-ii/credits/playstation-4/
- VGC on navigation patent: https://www.videogameschronicle.com/news/gta6-npc-improvements-patent/
- Press Start on locomotion patent: https://press-start.com.au/news/2023/10/30/gta-6-looks-to-be-getting-super-realistic-animation-tech-in-a-newly-discovered-rockstar-patent/
- GDC 2021, RDR2 horses (Kleanthous): https://gdcvault.com/play/1027230/AI-Summit-Making-the-Believable
- NaturalMotion ownership (Companies House 04304578): https://find-and-update.company-information.service.gov.uk/company/04304578
