---
class: Note
pinned: true
published: true
editing: true
topic:
  - "[Video Games](Video%20Games.md)"
created: 2023-11-10
modified: 2023-12-13
tags:
  - Video Games
---



# Current Bugs

- Crouching tag gate is broken.
- Dashing direction is inconsistent on repeated dashes.
- Consumption Pool System clamping is not accurate (double check)
- Mouse scrolling to change from first to third person breaks the camera toggle hotkey. Systems need unification.

# To Do

- Set up version control on Github.
- Convert dashing to use Add Force instead of Set Location
- Fix camera system.
- Make everything work in first and third person.
- Make the dash not suck when dashing on slopes
- Update Charge System debug messaging to match the style of the Consumption Pool System.
- Create generic map of debug message toggles.
- Create Consumption Pool modifier volumes like the pain causing volume, but for any Consumption Pool.
- Continuous jumping w/ bunny hopping (velocity acceleration)
- Crouch slide
- Wall running
- Grappling hook
- Zipline
- Remove setting vault height from event tick, put directly into vaulting execution flow
- Options & keybinds menu

# Implemented

- User Interface
	- Basic Main Menu
		- Navigate to/from gameplay area
	- Basic Escape Menu
		- Return to game, go to main menu, quit game.
	- Basic Heads Up Display
		- Updates according to the Consumption Pool System
		- Diablo-style design
- Gameplay Tag State Machine
	- Limits events and input actions based on current tags.
	- Tables for developer tools, player states, and movements states.
- Player Locomotion
	- Infinite Sprinting
		- Hold to sprint only at the moment.
		- Set up to consume the Stamina Consumption Pool by default.
			- Only consumes Stamina in combat.
	- Infinite Jumping
		- Set up to consume Charges *and* the Stamina Consumption Pool by default.
			- Limited to three Charges by default, so three jumps.
			- Only consumes Stamina in combat.
	- Infinite Dashing
		- Set up to consume the Stamina Consumption Pool by default.
			- Always consumes Stamina, even out of combat.
		- Lateral dashing only, not affected by camera pitch.
		- Dash forward by default when there's no movement input.
- Charge Pool System
	- The Charge Pool system limits the number of times any input action is fired by requiring the input action to consume from a limited Charge Pool.
	- Designed for a single input action that requires its own consumption pool.
- Consumption Pool System
	- The Consumption Pool System limits the number of times any input action is fired by requiring the input action to consume from a limited Consumption Pool.
	- Designed for multiple input actions that require a shared consumption pool.
	- Allows for unlimited enumerated Consumption Pools, with passthrough to the HUD UI.
		- Health, Mana, & Stamina Consumption Pools created by default.
	- Consumption Pools can dynamically change capacity, so all input actions that consume a Consumption Pool will scale as the capacity rises or falls.
	- Consumption Pool modification regeneration is allowed or disallowed based combat status.
	- Works as one-shot or using Delta Seconds.

# Vertical Slice Map

![Foglight 1.png](../attachments/Foglight%201.png)

# Inspirations

## Games

- Doom: Eternal / Postal: Brain Damaged
	- Immaculate boomer shooter combat
	- High focus on mobility
	- High skill ceiling
	- Unique weapons
- Runescape
	- Classless progression
	- Gearing is easy to understand
	- Large number of skills to progress
- EVE Online
	- Socially driven, political PvP with player defined "success" and "loss"
	- Player groups exist as spoken agreement
- Caves of Qud
	- Unusual approach to RPG archetypes
	- Systems-based gameplay design drives discovery
	- Procedurally assisted world with fixed landmarks, locations, and biomes
- Dark Souls
	- Overarching worldbuilding & lore
	- Has no true gear progression, instead has gear choices
- Elden Ring
	- Tree (Yggdrasil)
- Moonring
	- Shifting fog of terror
- Metro Series
	- Large subterranean areas as refuge from the surface
- S.T.A.L.K.E.R. Series
	- The world itself is your primary enemy
	- Exclusion zones & anomalies
- Final Fantasy
	- Fucking crystals, dude. Or rocks, in this case. Same shit.

## Books

- The Dark Tower Series, Stephen King
- Seventh Tower Series, Garth Nix
	- Sunstones as a source of power

# Monetization

- Buy to play only.
- Free updates, never pay for content.
- No micro-economy, ever. I hate it, and so do you.
- Localized pricing, I care more about your access to the game than how much money it makes me.

# Design Pillars

1. The game mechanics must be easy to understand.
2. The game must have a high mechanical skill ceiling.
3. World building should be visually and mechanically apparent.
4. The game should always respect the players' intelligence, period.
	- Everything is earnable through playing the game.
	- Goals and achievements are player-defined and based on ambition.
	- There is no player level or stat sheet. Ability is determined by specializing in skill trees which offer differing mechanical utilities. There is no power scaling, only learning mechanics, and being better at them than the next player.
	- There are no item levels, stat sheets, rarities, or RNG. All items are purpose built for a particular skill tree or hybrid of skill trees, and focus on providing unique mechanical utilities rather than redistributing stats like in most MMOs.
	- A piece of gear's utility scales with the progression of the respective skill trees, but doesn't require progression at all to be usable at a base level.
	- The game will never reward you with items out of thin air, only access to new combat or utility mechanics though skill progression.
	- The game will never stop you from making a bad decision, but we'll at least give you a heads up.
5. The threshold of "getting to the fun part" should be logging in to the game.
	- There will never be progression mechanics that rely on levels and gaining experience points, there will only be material or crafting costs.
	- There will never be time wasting mechanics. They suck, and usually serve to delay the realization that the game isn't all that fun to begin with.
6. PvP is *full loot* and *non-consensual*.
	- There is no PvP opt-out, and never will be.
	- PvP is socially driven instead of forced by game-defined participation requirements, rules, rewards, or win states.
7. The world itself is the meta-game, and each region interconnects vertically and spans the entirety of the play area. Each of these regions fundamentally change the primary game mechanics which drive exploration and player interaction, and reveal the lore of the world through natural deduction.

# World Building

## The World Tree

> It's us versus the world.

- The World Tree is the planet-bound equivalent of a cosmic deity, uncaring and unfeeling, only creating and destroying. It sprouted from a cosmic seed that drifted for eons before making landfall, long before living memory.
- The World Tree is home to many denizens, which dwell on the surface of its vast branches, occasionally forming small settlements.
- The World Tree spans the entire game map. As a result, the sun is only visible at its top-most branches.

## Fog

> Never assume sanity.

- Fog falls perpetually from the leaves of the World Tree, a storm of creative and destructive energy which drifts across the land, scouring and re-shaping everything it touches, acting as a primordial, chaotic force of manifestation. (Procedural Regeneration)
- Fog itself is the most important Consumption Pool, and is gathered and condensed down to form Fogstones, which emit light that wards the effects of Fog, known as Foglight.
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

> The road less taken, only because you must find it first.

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
- Fogstones are crafted through gathering and distilling Fog with specialized equipment. They can vary in size depending on the distillation period, similar to stalagmite formation.
- Fogstones require exposure to sunlight to be "born" after they have been crafted, otherwise they remain inert.
- Fogstones recharge by absorbing nearby natural light sources, dimming them or even snuffing them out in the process.
- Fogstones change color when in close proximity to Fog other Fogstones.
- Fogstones are naturally more radiant when farther from the sun.
- Fogstones are naturally more absorbent when closer the the sun.

### Fogstones vs Fog

- Fog cannot be dissipated by natural light like darkness can.
- The chaotic effects of Fog are only negated by Foglight.
- Everything which is unlit by Foglight will be scoured by Fog, which constantly roams the land and *changes* everything, procedurally destroying and creating areas completely anew.
- Everything which is lit by Foglight is left untouched by the effects of Fog, allowing players to create pockets of relative safety in which settlements, travel routes, Consumption Pool farms, and more may be formed.
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

# Player vs. Player

> Keep your friends close.

- This is a PvPvW game. The world is designed from the ground up to encourage players to kill each other. The goal is to create long-term social and political PvP, using the world as a strategic medium.
- PvP does not exist as game-defined rules, objectives, rewards, or win states. PvP sprouts from the ambitions of players and the natural risk vs. reward gameplay that the world creates through its inherently difficult and transient nature.
- Open world PvP creates natural distrust between players, while also creating an incentive to form unlikely parties based on the specialized abilities someone else can bring to the table.
- Fogstones and other light structures can be destroyed by other players at any time, and are the primary means of establishing routes for travel and trade, creating settlements and safe houses between major locations, and preventing Fog from destroying dungeons and Consumption Pool nodes so they can be used long term for skilling, economy, or war logistics. This becomes the primary vehicle for PvP.
- The world is difficult and widely unfriendly. Highly specialized allies ease the journey, but do not stop the clever solo player from hacking their own path through the wilderness.

# Dungeons

> Hold your ground.

- Dungeons are randomly created and destroyed within Fog storms.
- Dungeons offer a sort of settlement opportunity, with players contributing time and Consumption Pools to build up the difficulty and scale of the dungeon, as well as building greater defenses and weaponry to protect from other groups of players looking to control the area.
- Dungeons are not "cleared" but rather continuously spawn enemies that must be held at bay, and grow in scope the more they are progressed, making dungeons more akin to a growing Consumption Pool farm.

# Consumption Pool Acquisition

> Consumption Pools exist in the following forms:

- Mineable
- Harvestable
- Gatherable
- Craftable

# Gearing & Itemization

- Understanding gearing should be extremely straight forward.
- Every piece of gear should have infinite replay value.
- Gear should always be a tradeoff you make for particular encounters, environments, or economic reasons.
- Gear should never have an "item level" associated with it.
- NO item rarity on gear. Gear should serve a specific gameplay function that pertains to aiding or resisting each combat spec.
- All gear should be modifiable to increase build variety rather than vertical power progression, such as increasing resistances or modifying ability mechanics to suit different combat playstyles.

# Specialization

- Specs should never exist for the sake of existing. If it cannot be grounded in consequential gameplay, it should not exist.
- There should never be a spec limitation preventing players from completing every spec. (i.e. Runescape)
- The variety of specs should be wide enough and consequential enough to encourage players to pick a few to begin with.
- Every spec should offer a complete "way of life" and include abilities that have real utility across combat, economy, and exploration.
