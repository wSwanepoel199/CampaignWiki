---
NoteIcon: Settlement
Tags: Category/Settlement
Alignment: Chaotic Evil
name: Stagle
size: Small
type: City
region: Wilrania
Government: Autocracy
politics: Lordship
leader: 
defences:
guildsgroups:
 - Thieves Guild 1
 - Cult 1
 - Guiled 1
population: 8231
commonraces:
 - Humans
 - Elves
 - Dwarves
religion:
 - Lathander
exports: 
 - Nothin
imports: 
 - More Nothin
distToSharebrook: 120
distToFlater: 147
distToWilwood: 186
distToAngelham: 211
distToFlaywagoon: 225
distToShadow: 290
---

> [!infobox|txt-c wfit]
> # `=this.name`
> ![[stagle-map.svg|cover wfit hfit]]
> [[stagle-map.svg|Show To Players]]
> ###### Geography
> Type |  Stat |
> ---|---|
> Type | `=this.type` |
> Size | `=this.size` |
> Region | `=this.region` |
> ###### Travel (`=[[TravelConfig]].HoursPerDay` hrs/day)
> Destination |  Travel Days  |
> ---|---|
> [[Sharebrook]] | 🕓`VIEW[round({distToSharebrook} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Flater]] | 🕓`VIEW[round({distToFlater} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` | 
> [[Wilwood]] | 🕓`VIEW[round({distToWilwood} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Angelham]] | 🕓`VIEW[round({distToAngelham} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Flaywagoon]] | 🕓`VIEW[round({distToFlaywagoon} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> [[Shadow]] | 🕓`VIEW[round({distToShadow} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
> ###### Politics
> Type |  Stat |
> ---|---|
> Govt Type | `=this.politics` |
> Ruler | `=this.leader` |
> Defence | `=this.defences` |
> ###### Organizations
> Type |  Stat |
> ---|---|
> Guilds & Groups | `=this.guildsgroups` |
> ###### Society
> Type |  Stat |
> ---|---|
> Population | `=this.population` |
> Races | `=this.commonraces` |
> Temples | `=this.religion`  |
> ###### Commerce
> Type |  Stat |
> ---|---|
> Exports | `=this.exports` |
> Imports | `=this.imports` |


# `=this.name`

A small city that once sat on the border between the Kingdom of Slek and the Republic of Aslenasin. It lost must of its importance as the 100 year war raged on, struggling to draw new citizens and travellers even after the war ended.

## Overview
Placeholder

### Map of Stagle
![[Map of Stagle]]

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