---
NoteIcon: Settlement
Tags: Category/Settlement
Alignment: Chaotic Evil
name: Shadow
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
population: 12204
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
distToBronward: 120
distToSwanpoint: 206
distToFlater: 239
distToStagle: 290
distToFlaywagoon: 316
---

NewLocation


> [!infobox|txt-c wfit]
> # `=this.file.name`
> 
> ![[shadow-map.svg|cover wfit hfit]]
> [[shadow-map.svg|Show Full Image]]
> 
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
> [[Bronward]] | 🕛`VIEW[round({distToBronward} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
> [[Swanpoint]] | 🕛`VIEW[round({distToSwanpoint} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
> [[Flater]] | 🕛`VIEW[round({distToFlater} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
> [[Stagle]] | 🕛`VIEW[round({distToStagle} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
> [[Flaywagoon]] | 🕛`VIEW[round({distToFlaywagoon} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`|
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

### Map of Shadow

![[Map of Shadow]]

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