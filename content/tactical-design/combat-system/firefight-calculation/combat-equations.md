---
title: "Overall Combat Equations"
type: index
weight: 4
---

## Nomenclature

- `hard attack modifier`: `0-100%` (HAM)
- `soft attack modifier`: `0-100%` (SAM)
- `accuracy attack modifier`: `0-100%` (AAM)
- `training attack modifier`: `0-100%` (TAM)
- `hard defense modifier`: `0-100%` (HDM)
- `soft defense modifier`: `0-100%` (SDM)
- `entrenchment defense modifier`: `0-100%` (EDM)
- `training defense modifier`: `0-100%` (TDM)
- `Soft Attack` (Sa)
- `Hard Attack` (Ha)
- `Accuracy Attack` (Aa)
- `Training Attack` (Ta)
- `Soft Defense` (Sd)
- `Hard Defense` (Hd)
- `Entrenchment Defense` (Ed)
- `Training Defense` (Td)
- `gen supply` (Sg)
- `gen coordination` (Cg)
- `gen speed` (Spg)
- `gen size` (sg)
- `battles fought` (bg)
- `attack roll` (AR)
- `defense roll` (DR)
 
## Attack Equations

- If attacking an `unarmored` target
    - `AS = ((0.2*HAM*Ha)+(0.8*SAM*Sa))+(AAM*Aa)+(TAM*Ta)`

- If attacking an `armored` target
    - `AS = ((0.2*SAM*Sa)+(0.8*HAM*Ha))+(AAM*Aa)+(TAM*Ta)`

## Defense Equations

- If defending from an `unarmored` target
    - `DS = ((0.2*HDM*Hd)+(0.8*SDM*Sd))+(EDM*Ed)+(TDM*Td)`

- If defending from an `armored` target
    - `DS = ((0.2*SDM*Sd)+(0.8*HDM*Hd))+(EDM*Ed)+(TDM*Td)`

## General Equations

- General Score (GS)
- `GS = Sg+Cg+Spg`
    - `Cg = ((Sg+sg-bg)-100)/100`
    - `Spg = ((Cg-sg)-100)/100`

## Firefight Score

- For attackers (FSa):
    - `FSa = AS + GS`
- For defenders (FSd):
    - `FSd = DS + GS`


## Putting Everything Together

Four firefight options (attack v defense):

- armor v armor
    - `1`
- armor v soft
    - `2`
- soft v armor
    - `3`
- soft v soft
    - `4`

#### 1

- `FSa = ((0.2*SAM*Sa)+(0.8*HAM*Ha))+(AAM*Aa)+(TAM*Ta) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`
- `FSd = ((0.2*SDM*Sd)+(0.8*HDM*Hd))+(EDM*Ed)+(TDM*Td) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`

Final Result:

- `(AR*FSa)` vs `(DR*FSd)`

#### 2

- `FSa = ((0.2*HAM*Ha)+(0.8*SAM*Sa))+(AAM*Aa)+(TAM*Ta) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`
- `FSg = ((0.2*SDM*Sd)+(0.8*HDM*Hd))+(EDM*Ed)+(TDM*Td) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`

Final Result:

- `(AR*FSa)` vs `(DR*FSd)`

#### 3

- `FSa = ((0.2*SAM*Sa)+(0.8*HAM*Ha))+(AAM*Aa)+(TAM*Ta) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`
- `FSd = ((0.2*HDM*Hd)+(0.8*SDM*Sd))+(EDM*Ed)+(TDM*Td) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`

Final Result:

- `(AR*FSa)` vs `(DR*FSd)`

#### 4

- `FSa = ((0.2*HAM*Ha)+(0.8*SAM*Sa))+(AAM*Aa)+(TAM*Ta) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`
- `FSd = ((0.2*HDM*Hd)+(0.8*SDM*Sd))+(EDM*Ed)+(TDM*Td) + Sg + (((Sg+sg-bg)-100)/100) + (((Cg-sg)-100)/100)`

Final Result:

- `(AR*FSa)` vs `(DR*FSd)`