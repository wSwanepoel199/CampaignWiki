---
NoteIcon: map
---

```leaflet   
### id must be unique  
id: axirune_map
### Lock pins so they can't be moved  
lock: true  
### If true, view of map will recenter as you zoom out.  
recenter: false
### If true, disables mouse scroll for zomming in and out of a map. Button controls still work.  
noScrollZoom: false  
image: [[Axirune-map.svg]]
### Map Pixel Height x 1 / (Pixels between Bar Scale / 100)  
### Map Pixel Width x 1 / (Pixels between Bar Scale / 100)  
### Note that this formula requires adjustments depending on your map. The idea is to determine the number of units between your bar scale. We divide by 100 here because my bar scale measures in 100 units. If your maps scale bar measures in units of 50 them you should divide by 50 instead. The idea is to calculate how many pixels are equal to 1 unit.  
### Bounds is entered as [Height, Width]  [1297, 2560]
bounds: 
- [0,0]
- [1284.158,2534.653]  
height: 500px  
width: 95%  
### This sets where the map starts by default. Set it to the middle (half) of your bounds.  
lat: 642.079
long: 1267.327
### 0 is no zoom. Negative zoom steps away from the map. Positive zoom steps towards the map.  
minZoom: 1
### Max zoom is 18.  
maxZoom: 6
### Hover mouse over the Reset Zoom icon to see your current zoom level.  
defaultZoom: 1
### How far it zooms in or out with each step. Can be in decimals.  
zoomDelta: 0.5  
### This is a string so can be any text. Change it to match your maps measurement scale.  
unit: miles  
scale: 4.05
darkMode: false
marker: 
 - Capitol,565.6592,1607.3017,Fraystalde,,,
 - Settlement,550.7754,1572.5699,Swanpoint,,2.5,
 - Settlement,559.7503,1535.1788,Shadow,,2.5,
 - Settlement,585.6702,1509.1903,Stagle,,2.5,
 - Settlement,622.4595,1487.5806,Wilwood,,2.5,
 - Capitol,764.2129,1287.7048,Ysenas,,,
```