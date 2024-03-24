---
NoteIcon: map
---

```leaflet
### Tutorial: [https://youtu.be/54EyMzJP5DU](https://youtu.be/54EyMzJP5DU)  
### preserveAspect: true
### id must be unique  
id: ysenas_map
### Lock pins so they can't be moved  
lock: false  
### If true, view of map will recenter as you zoom out.  
recenter: false
### If true, disables mouse scroll for zomming in and out of a map. Button controls still work.  
noScrollZoom: false  
image: [[ysenas-map-noui.svg]]
### Map Pixel Height x 1 / (Pixels between Bar Scale / 100)  
### Map Pixel Width x 1 / (Pixels between Bar Scale / 100)  
### Note that this formula requires adjustments depending on your map. The idea is to determine the number of units between your bar scale. We divide by 100 here because my bar scale measures in 100 units. If your maps scale bar measures in units of 50 them you should divide by 50 instead. The idea is to calculate how many pixels are equal to 1 unit.  
### Bounds is entered as [Height, Width]  [911, 1041]
bounds: 
 - [0,0]
 - [2777.439,3173.78]
height: 500px  
width: 100%  
### This sets where the map starts by default. Set it to the middle (half) of your bounds.
lat: 1388.72
long: 1586.89
### 0 is no zoom. Negative zoom steps away from the map. Positive zoom steps towards the map.  
minZoom: -2.5
### Max zoom is 18.  
maxZoom: 2.5
### Hover mouse over the Reset Zoom icon to see your current zoom level.  
defaultZoom: -2.5
### How far it zooms in or out with each step. Can be in decimals.  
zoomDelta: 0.5 
### This is a string so can be any text. Change it to match your maps measurement scale.  
unit: meters 
scale: 1
darkMode: false
marker: 
 - default,1404.7118,1186.6942,[[Ysenas#House of Representatives|House of Representatives]],,0,
# - default,5,3.25,0,,,
# - default,5,57.25,5,,,
```

^d641a6
