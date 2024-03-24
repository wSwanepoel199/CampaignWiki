---
NoteIcon: Settlement
Tags: Category/Settlement
Alignment: Chaotic Evil
title: Settlement
size: Small
type: Settlement
region: 
 - This area
 - Of this area
Government: Autocracy
politics: Lordship
leader:
defences:
guildsgroups:
 - Thieves Guild 1
 - Cult 1
 - Guiled 1
population: 0
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
distToNeighbour: 0
---

<% tp.file.title %>
<% await tp.file.move("/Axirune/1. The World/World/" + tp.file.title) %>

<%*
const hasTitle = !tp.file.title.startsWith("NewLocation");
let title;
if (!hasTitle) {
    title = await tp.system.prompt("Enter Settlement Name");
    await tp.file.rename(title);
} else {
    title = tp.file.title;
}
_%>

> [!infobox|txt-c wfit]
> # `=this.file.name`
> ![[z_Assets/Misc/MapPlaceholder.png|cover hsmall wsmall]]
> [[z_Assets/Misc/MapPlaceholder.png|Show To Players]]
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
> [[Voonlar]] | 🕓`VIEW[round({distToNeighbour} / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]` |
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
![[z_Assets/Misc/MapPlaceholder.png|Placeholder Map]]
[[z_Assets/Misc/MapPlaceholder.png|open outside]]

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