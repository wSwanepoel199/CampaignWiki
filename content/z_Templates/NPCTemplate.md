---
NoteIcon: npc
title:
associatedGroup: 
gender: 
race: 
age: 
class: 
alignment: 
characterRole: 
location: 
---

<% tp.file.title %>
<% await tp.file.move("/Axirune/1. The World/World/Non Player Characters/" + tp.file.title) %>

<%*
const hasTitle = !tp.file.title.startsWith("NewNPC");
let title;
if (!hasTitle) {
    title = await tp.system.prompt("Enter NPC Name");
    await tp.file.rename(title);
} else {
    title = tp.file.title;
}
_%>

> [!infobox| txt-c]
> # `=this.file.name`
> ![[z_Assets/Misc/ImagePlaceholder.png|cover hsmall]]
> [[z_Assets/Misc/ImagePlaceholder.png|Show To Players]]
> ###### Basic Information
> Type |  Stat |
> ---|---|
> Home | `=this.location` |
> Group | `=this.associatedGroup` |
> Sex | `=this.gender` |
> Race | `=this.race` |
> Age | `=this.age` |
> Condition | Healthy |
> ###### Rules Info
> Type |  Stat |
> ---|---|
> Alignment | `=this.alignment` |
> Class | `=this.class` |
> Character Role | `=this.characterRole` |
> ###### Quick Stats
> Stat | Value |
> ---|---|
> Armor Class | 

# `=this.file.name`
## Profile

<% tp.file.cursor() %>
**<Add description here, extend it with AI Text Generator using Ctrl J>**

> [!info]+ Statblock
> ```statblock
> name: Individual
> monster: Commoner
> columns: 1
> ```

```encounter-table
name: Individual
creatures:
 - 1: Commoner
```