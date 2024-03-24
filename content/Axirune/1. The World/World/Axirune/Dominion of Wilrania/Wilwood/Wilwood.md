---
NoteIcon: Settlement
Tags: Category/Settlement
Alignment: Chaotic Evil
name: Wilwood
size: Medium
type: Town
region: Wilrania
Government: Autocracy
politics: Lordship
leader:
defences:
guildsgroups:
 - Thieves Guild 1
 - Cult 1
 - Guiled 1
population: 1801
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
distToAngelham: 45
distToStagle: 186
distToSharebrook: 244
distToWilran: 279
distToBearbor: 504
---

NewLocation


> [!infobox|txt-c wfit]
> # `=this.file.name`
> ![[wilwood-map.svg|cover wfit hfit]]
> [[wilwood-map.svg|Show To Players]]
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
> [[Angelham]] | 🕓`VIEW[round({distToAngelham} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Stagle]] | 🕓`VIEW[round({distToStagle} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Sharebrook]] | 🕓`VIEW[round({distToSharebrook} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Wilran]] | 🕓`VIEW[round({distToWilran} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Bearbor]] | 🕓`VIEW[round({distToBearbor} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
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

### Placeholder Map

![[Map of Wilwood]]

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