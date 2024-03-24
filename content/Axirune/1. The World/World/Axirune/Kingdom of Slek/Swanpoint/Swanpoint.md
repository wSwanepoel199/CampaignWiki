---
NoteIcon: Settlement
Tags: Category/Settlement
Alignment: Chaotic Evil
name: Swanpoint
size: Medium
type: City
region: Slek
Government: Autocracy
politics: Lordship
leader:
defences:
guildsgroups:
 - Thieves Guild 1
 - Cult 1
 - Guiled 1
population: 10626
commonraces:
 - Humans
 - Elves
 - Dwarves
religion:
 - Lathander
exports: 
 - Something
imports: 
 - Something Else
distToFraystalde: 171
distToShadow: 206
---

NewLocation


> [!infobox|txt-c wfit]
> # `=this.file.name`
> ![[swanpoint-map.svg|cover wfit hfit]]
> [[swanpoint-map.svg|Show Full Image]]
> ###### Geography
> Type |  Stat |
> ---|---|
> Type | `=this.type` |
> Size | `=this.size` |
> Region | `=this.region` |
> 
> ###### Travel (`=[[TravelConfig]].HoursPerDay` hrs/day)
> Destination |  Travel Days  |
> ---|---|
> [[Fraystalde]] | 🕛`VIEW[round({distToFraystalde} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
> [[Shadow]] | 🕛`VIEW[round({distToShadow} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
> 
> ###### Politics
> Type |  Stat |
> ---|---|
> Govt Type | `=this.politics` |
> Ruler | `=this.leader` |
> Defense | `=this.defences` |
> 
> ###### Organizations
> Type |  Stat |
> ---|---|
> Guilds & Groups | `=this.guildsgroups` |
> 
> ###### Society
> Type |  Stat |
> ---|---|
> Population | `=this.population` |
> Races | `=this.commonraces` |
> Temples | `=this.religion`  |
> 
> ###### Commerce
> Type |  Stat |
> ---|---|
> Exports | `=this.exports` |
> Imports | `=this.imports` |


# `=this.file.name`
## Overview
Placeholder

### Map of Swanpoint

![[Map of Swanpoint]]

### Placeholder Picture
![[z_Assets/Misc/ImagePlaceholder.png|Placeholder Picture]]
[[z_Assets/Misc/ImagePlaceholder.png|open outside]]

Placeholder

## Notable NPCs
Placeholder

## Profile
Placeholder

## Story
Placeholder

## Points of Interest
Placeholder

## Valuables
Placeholder

## Internal Relationships
Placeholder

## Outward Relationships
Placeholder

## Background
Placeholder

## Additional Details
Placeholder

`=this.region`


`=link(this.region)`