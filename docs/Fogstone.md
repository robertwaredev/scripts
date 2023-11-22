---
class: Note
pinned: true
published: true
editing: true
topic:
  - "[Video Games](Video%20Games.md)"
created: 2023-11-10
modified: 2023-11-22
tags:
  - Video Games
---



![Foglight.png](../attachments/Foglight.png)

# Inspirations

- Doom: Eternal / Postal: Brain Damaged
	- Immaculate boomer shooter combat
	- High focus on twitch mobility
	- High skill ceiling
- Runescape
	- Simple gearing
	- Classless progression
	- Large number of skills to progress
- EVE Online
	- Social, political PvP with player defined "success" and "loss"
- Caves of Qud
	- Systems-based mechanics drive gameplay and discovery
	- Procedurally assisted world with fixed landmarks, locations, and biomes
	- Unusual approach to RPG archetypes
- Dark Souls
	- Skill > Gear
	- Has no true gear progression, instead has gear choices
	- Perfect worldbuilding & lore
- Elden Ring
	- Tree
- 2B2T Minecraft Server
	- Systems are meant to be abused
	- The ambition of players fundamentally reshapes the game space
	- Player groups exist only as spoken agreements, rather than through an in-game party or guild mechanic
- Moonring
	- Shifting fog of terror
- Metro Series
	- Large subterranean areas as refuge from the surface
- S.T.A.L.K.E.R. Series
	- The world itself is your primary enemy
	- Exclusion zones & anomalies
- Final Fantasy
	- Fucking crystals, dude.

# Design Pillars

> For the record.

- The game should be extremely simple to understand, yet have a high mechanical skill ceiling.
- Rewards should always be based on how much risk you take.
- PvP cannot be turned off, go fuck yourself. PvP is *not* a game mode or a server type, it's a foundational design pillar upon which the world building and absolutely everything else rests.
- Game mechanics should be systematic and encourage socially driven PvP instead of game-defined rules or "win" states.
- World building and lore should be steeped and visually apparent, but a "main story quest" should not be required to understand the game or play it at a high level.
- The *entire world space* is the main meta-game, with the three main regions each forcing you to use the fundamental mechanics in drastically different ways to deal with the challenges that come with each. Due to these regions being vertically stacked on top of each other, rather than next to each other as on a typical game map, all three areas have mechanics that affect the others directly.

# World Building

> It's us versus the world.

## The World Tree

- The World Tree is the planet-bound equivalent of a cosmic deity, uncaring and unfeeling, only creating and destroying. It sprouted from a cosmic seed that drifted for eons before making landfall, long before living memory.
- The World Tree is home to many denizens, which dwell on the surface of its vast branches, occasionally forming small settlements.
- The World Tree spans the entire game map. As a result, the sun is only visible at its top-most branches.

## Fog

> Never assume sanity.

- Fog falls perpetually from the leaves of the World Tree, a storm of creative and destructive energy which drifts across the land, scouring and re-shaping everything it touches, acting as a primordial, chaotic force of manifestation. (Procedural Regeneration)
- Fog itself is the most important resource, and is gathered and condensed down to form Fogstones, which emit light that wards the effects of Fog, known as Foglight.
- Fog comes with the challenge of hallucinations, shifting environments, randomly mutated enemies, spontaneous player translocation, wormhole apparition, temporary quantum entanglement, evil twins from parallel universes, and much more.
- Fog is made up of many "exclusion zone" style storms that roam the land, and is only survived by the most knowledgeable and well-prepared.

## Light & Dark

> Wicked things this way come.

- Light sources exist in two forms: natural light, and Foglight.
- Enemies, anomalies, and other disturbances emerge in the absence of natural light.
- Sunlight wards off darkness, but burns the bare skin of players, and can't be survived for long periods of time without sufficient resistant gear.
- Gentler natural light sources also ward off darkness, and are produced by fire or bioluminescence.
- Foglight wards off darkness *and* neutralizes the effects of Fog in a localized area.
- Both types of light sources exist as a variety of carried items, worn items, and buildable structures.

## The Overworld

> A shifting, unpredictable realm.

- The Overworld is completely absent of sunlight, blocked out by the many branches of the World Tree.
- Enemies, anomalies, and other disturbances are constantly emerging from the darkness.
- Fog storms also roam the Overworld, destroying and creating new areas as they move, as well as causing a variety of unpredictable effects.

## Fog Gates

- Fog Gates are passages between the Overworld and The Old World, destroyed and created in new locations with the passing of the Fog. They are the only means of accessing The Old World.

## The Old World

> Don't get lost.

- The Old World is a massive, subterranean cave network made up of the spaces left behind by ruined cities and the rotting roots of the World Tree. No sunlight reaches the Old World.
- Enemies, anomalies, and other disturbances are constantly emerging from the darkness.
- The Overworld has a multitude of passages to the Old World which are created and destroyed in the Fog at random locations. These passages remain either until the Fog returns to scour them from the face of the map, or players protect them by building Foglight structures that ward off the Fog.
- Fog does not penetrate very deep into the Old World, thus the Old World remains a largely unchanged gameplay space, save for the shifting passages leading to the Overworld.

## Fogstones & Foglight

> Order in chaos, and chaos in order.

- Fogstones produce Foglight, the only thing capable of negating the effects of Fog.
- Unlike natural light sources, Fogstones never fully expire, only dim to a minimum light level.
- Fogstones recharge by absorbing natural light sources, dimming them or even snuffing them out, with the only exception being the sun.
- Fogstones are naturally more radiant at a base level when in close proximity to Fog other Fogstones.
- The natural properties of Fogstones change with elevation, more on that below.

### Fogstones vs Fog

> Cosmic horrors beyond human comprehension.

- Fog cannot be dissipated by natural light like darkness can.
- The chaotic effects of Fog are only negated by Foglight.
- Everything which is unlit by Foglight will be scoured by Fog, which constantly roams the land and *changes* everything, procedurally destroying and creating areas completely anew.
- Everything which is lit by Foglight is left untouched by the effects of Fog, allowing players to create pockets of relative safety in which settlements, travel routes, resource farms, and more may be formed.
- As a Fog dweller, you'll have to roll without using Fogstones if you want the high rewards for your high risk, using only expendable light sources to guide you, if any light at all.

### Fogstones vs Overworld

- Due to the abundance of Fog on surface of the Overworld, Fogstones are naturally more radiant there, resonating positively with their unrefined state of matter, as if calling out for their home.
- On the Overworld, Fogstones can act as a navigational aid in finding or avoiding Fog when carried, a harbinger of encroaching Fog when built as structures such as street lamps or lighthouses, and importantly, an unfortunate beacon in the night for other players looking to profit on your misery.

### Fogstones vs Old World

- In the Old World, Fogstones have an increased radiance the deeper you go, and a reduced ability to absorb natural light to recharge.
- Civilization has attempted to rebuild here, free from the effects of Fog, but far from the sunlight necessary to keep darkness more than a stone's throw away. Old World settlements rely heavily on using significant amounts of natural light, like bonfires, or by converting it into perpetual Foglight through Fogstone absorption.

### Fogstones vs World Tree

- In the World Tree, Fogstones have a reduced radiance the higher you go, and an increased ability to absorb natural light to recharge.
- The World Tree is dark, difficult, and dangerous to traverse, but provides substantial payoff when you make it to the top branches and recharge your Fogstones.

# Player Interactions

> Keep your friends close.

- This is a PvPvW game. The primary world design from the ground up is to encourage players to kill each other. The goal is to create long-term social and political PvP, using the world as a strategic medium.
- PvP does not exist as game-defined rules or objectives. PvP sprouts from the ambitions of players and the natural risk vs. reward gameplay that the world creates through its inherently difficult and transient nature.
- Open world PvP creates natural distrust between players, while also creating an incentive to form unlikely parties based on the specialized abilities someone else can bring to the table.
- Fogstones and other light structures can be destroyed by other players at any time, and are the primary means of establishing routes for travel and trade, creating settlements and safe houses between major locations, and preventing Fog from destroying dungeons and resource nodes so they can be used long term for skilling, economy, or war logistics. This becomes the primary vehicle for PvP.
- The world is difficult and widely unfriendly. Highly specialized allies ease the journey, but do not stop the clever solo player from hacking their own path through the wilderness.

# Dungeons

> Hold your ground.

- Dungeons are randomly created and destroyed within Fog storms.
- Dungeons offer a sort of settlement opportunity, with players contributing time and resources to build up the difficulty and scale of the dungeon, as well as building greater defenses and weaponry to protect from other groups of players looking to control the area.
- Dungeons are not "cleared" but rather continuously spawn enemies that must be held at bay, and grow in scope the more they are progressed, making dungeons more akin to a growing resource farm.

# Resource Acquisition

> Resources exist in the following forms:

- Mineable
- Harvestable
- Gatherable
- Craftable

# Character Building

- NO gender or race locking due to classless progression.

# Gearing & Itemization

- Understanding gearing should be extremely straight forward.
- Every piece of gear should have infinite replay value.
- Gear should always be a tradeoff you make for particular encounters, environments, or economic
- Gear should never have an "item level" associated with it.
- NO item rarity on gear. Gear should serve a specific gameplay function that pertains to aiding or resisting each combat spec.
- All gear should be modifiable to increase build variety rather than vertical power progression, such as increasing resistances or modifying ability mechanics to suit different combat playstyles.

# Specialization

- Specs should never exist for the sake of existing. If it cannot be grounded in consequential gameplay, it should not exist.
- There should never be a spec limitation preventing players from completing every spec. (i.e. Runescape)
- The variety of specs should be wide enough and consequential enough to encourage players to pick a few to begin with.
- Every spec should offer a complete "way of life" and include abilities that have real utility across combat, economy, and exploration.
