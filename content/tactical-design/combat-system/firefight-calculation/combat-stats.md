---
title: "Combat Statistics"
type: index
chapter: false
weight: 2
---

Statistics determine the outcome of `firefights`, and are thus very important

## Main Stats

- These are 'base stats'
- All main stats have a range of `0-100`
- `combat` and `general`
    - combat stats: `attack`, `defense`, `range`
    - `combat` stats determine engagements 
    - Attack Order defined in [attack order](#attack-order)
        - determines `attack` and `defense`
        - change based on troop level
    - `range` has base stat from unit type && unit level
        - split up into zones. Units have cones of vision, and the cone is split up into arc sections.
            - each arc section is a 'roll slot' on the firefight dice modifier
            - the closer you are, the more roll slots you have
                - the more info you have on the enemy and their movements, the better aim you have, the better you can maneuver, etc.
    - `general` stats are strategic 
        - `supply`
        - `coordination`
            - change based on strategy
        - `speed`
            - change based on troop type + size
        - `size`
            - changes by troop type
- explained further in combat-stats
- stat `keys` are rigid, and *all* troops have the same, regardless of type
    - `attack`, `defense`, `supply`, `coordination`
- stat `values` change over time
    - the actual value of the stat (aka `key`)

#### Attack Stats

- Defender-based
    - `Soft Attack` (S)
        - Attack stat against Infantry, unarmored buildings, unarmored vehicles
    - `Hard Attack` (H)
        - attack stat against armored vehicles and buildings
- `Accuracy` (A)
    - "Ability to hit shots"
- `Training` (T)
    - "Ability to stay calm under pressure and communicate"

###### Attack Scoring

If a troop is `attacking`, then a `attack score` (AS) will be calculated at the end of the firefight.

The AS (and DS) are maximum `300`

A troop can either be attacking an `armored` or an `unarmored` target

- If attacking an `unarmored` target
    - `AS = x((0.2*H)+(0.8*S))+xA+xT`
- If attacking an `armored` target
    - `AS = x((0.2*S)+(0.8*H))+xA+xT`


#### Defense Stats

- Attacker-based
    - `Soft Defense` (S)
        - ability to defend against infantry and their maneuvering
        - ability to defend against small arms
    - `Hard Defense` (H)
        - ability to defend against armored vehicles and their maneuvering
        - ability to defend against artillery/explosions
- `Entrenchment` (E)
    - "ability to 'hold your ground' and not maneuver"
- `Training` (T)
    - "ability to stay calm under pressure and communicate"

###### Defense Score

If a troop is `defending`, then a `defense score` (DS) will be calculated at the end of the firefight.

A troop can either be defending from an `armored` or an `unarmored` attacker

The DS (and AS) are maximum `300`

- If defending from an `unarmored` target
    - `DS = ((0.2*xH)+(0.8*xS))+xE+xT`
- If defending from an `armored` target
    - `DS = ((0.2*xS)+(0.8*xH))+xE+xT`

###### x

x is the stat modifier, explained more in the combat-modifiers page

#### General Stats

- `supply` (S)
    - comes from the strategic situation, supply calculations for troops discussed in the `strategy design` section
    - `0-100`
- `coordination` (C)
    - similar to training, this is general coordination
    - changes over time based on battles seen, supply and size
        - over time, coordination goes down
            - each firefight removes 1 coordination
                - can be regained by resting
        - the bigger the unit, the lower the coordination
    - `0-100`
- `speed` (Sp)
    - This is 'unit speed', and pertains to the unit's ability to maneuver between firefights
    - is _not_ map movement speed
    - `0-100`
- `size` (s)
    - unit size, determines the amount of firefights the unit can lose
    - `1-15`

###### General Score

- General Score (GS)
    - `GS = S+C+Sp`
        - `C = ((S+s-b)-100)/100`
        - `Sp = ((C -s)-100)/100`


## Total Firefight Score

Firefight Score (FS) is the sum of Attack/Defense and General Score (not including modifiers)

- For attackers:
    - `FS = AS + GS`
- For defenders:
    - `FS = DS + GS`