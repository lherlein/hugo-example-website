---
title: "Combat Modifiers"
type: index
weight: 3
---

Here, attack modifiers are discussed

## Modifiers 

- not rigid, change troop to troop, scenario to scenario
- modifiers are percentage based
- applied after the main stat equations are computed
- modifiers are based on multiple things
    - some modifiers come from troop type
        - ex: `special forces` have `training +4%` and `accuracy +2%` (both attack modifiers)
    - some modifiers come from situations
        - ex: `special forces` have "+6% attack in mountains" and "+3% defense in forest"
    - dice modifier is random

### Attack/Defense Modifiers

For each of the 4 attack/defense statistics, there is a modifier in the form of a percentage. 

- `hard attack modifier`: `0-100%` (HAM)
- `soft attack modifier`: `0-100%` (SAM)
- `accuracy attack modifier`: `0-100%` (AAM)
- `training attack modifier`: `0-100%` (TAM)

- `hard defense modifier`: `0-100%` (HDM)
- `soft defense modifier`: `0-100%` (SDM)
- `accuracy defense modifier`: `0-100%` (ADM)
- `training defense modifier`: `0-100%` (TDM)

### "Dice" Roll Modifiers

Once a firefight 'final score' (FS) is calculated (based on combat-stats equations), then 'two five sided dice' (random number (0-9)) are rolled. The outcome becomes an extra `modifier` (see [modifiers](#modifiers)).

| Roll | Modifier |
|------|----------|
| 0    | +20%     |
| 1    | +12%     |
| 2    | +10%     |
| 3    | +8%      |
| 4    | +5%      |
| 5    | +5%      |
| 6    | +8%      |
| 7    | +10%     |
| 8    | +12%     |
| 9    | +20%     |

- Range of rolls available is based on the unit's `supply` and `range`.
- if total attack order modifier `>10%`, + 1 roll slot

##### Roll Window

- Roll window is the amount of possible numbers you can roll.
    - starts from the 'inside out'
    - lower number means you can only roll more likely numbers
        - ex: roll window of 2 means you can only roll 4 and 5
        - ex: roll window of 8 means you can roll 1-8
        - ex: roll window of 5 means you can roll 2-6
- Roll window is based on the unit's supply and range.
    - supply split into 5 20% sections
        - 0-20% = 1 window, 21-40% = 2 windows, etc.
    - units have max range, and vision 'cone'
    - vision cone split into 5 'arc sections'
    - 'range' window is based on which arc section the enemy unit falls into when the firefight begins
        - On attack: the farther away, the lower the attack window
            - farthest arc section: roll window = 1, etc.
        - On defense, the opposite of the above is true
        
- roll window cannot go above 10