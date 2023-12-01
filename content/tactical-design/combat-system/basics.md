---
title: "Basics of Battlefield-Level Tactical Control"
type: index
weight: 2
---

## Control

- Battlefields are layed out as 2D maps. 
- `Combat Group`s (CG) are shown as sprites on the map. 
    - Known/Suspected enemy CGs are on the map in red
    - friendly CGs are in green
- Any CG can be selected to show information on it
- Friendly selected units can be moved to a location by `right-click`
- Friendly units can `engage` the enemy using a button placed on the screen
    - See the [engage mechanic]() page for more info on the mechanic
- As units move around the map and `engagements` begin, enemy units will maneuver based on evaluated outcome of their movement 
    - a lot like a chess engine

## Time

- Time passes on the battlefield similar to a Paradox Interactive game
- Activity is assessed in '2 minute' increments
    - Can be considered a game tick
    - speed of ticks passing can be sped up or slowed down 
        - 1-5 scale of time speed, 5 being fastest

## Combat

Combat is broken down into `engagements` and `firefights`

- Engagement
    - `Combat Group` combat
        - 'Overall Fight'
    - Happens when opposing units clash
    - Lasts Z amount of time based on the amount of troops engaged, terrain, momentum.
        - This time value will be determined later
    - Troops can attempt to move or `re-engage` when the engagement is over (Z time has passed)
        - re-engagement starts another `engagement`
    - [Combat groups](#combat-groups) can move only after engagements are complete
- Firefight
    - `fireteam` combat
        - 'Individual Fights'
    - Last *exactly* 2 minutes of in-game time
        - b/c of this, the amount of `firefights` per `engagement` varies based on `engagement` time
    - Determines casualties, vehicle and infantry
        - Find 'combat-units' for information on troop type
    - Outcome based on combat-stats combined with [Dice Roll Modifiers](#dice-roll-modifiers)
    - Attack-type units will attempt to close distance between firefights
        - distance closed is based on unit `speed`
    - Defense-type units will stay still