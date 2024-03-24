---
BaseSpeed: 30
SpeedMultiplier: 1
AdditionalBonus: 0
Encumbered: false
HorseshoesofSpeed: false
HoursPerDay: 8
MinutesPerMile: 20
ExhaustionLevel: 0
TravelDistance: 145
varMins: 60
ShipCostPerM: 5
MessengerCostPerM: 5
CoachCost: 2
CoachCostPerM: 5
DangerLevel: 3
FamiliarRoute: true
PartyMembers: 6
LifestyleCostSP: 1
IncludeMeals: true
TravelCalc: 3
---

# Travel Speed
Updating the calculator below will flows the changes out to any notes that automatically calculate the travel distance. You need to refresh this note in order to see calculated changes. 


**Travel Method:** `=this.TravelMethod`
**Current Movement Per Round** `=this.BaseSpeed`
**Hours of Travel Per Day** `=this.HoursPerDay`
**Exhaustion Level** `=this.ExhaustionLevel`

# Calculator

| DnD5e Travel Settings | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Select Base Speed:** `INPUT[inlineSelect(option(30, Walking), option(50, Camel), option(40, Donkey), option(40, Mule), option(40, Draft Horse), option(40, Elephant), option(40, Mastiff), option(40, Moorbounder), option(40, Pony), option(40, Rhinoceros), option(60, Riding Horse), option(40, Saber-Toothed Tiger), option(60, Warhorse), option(20, Griffon [walking]), option(80, Griffon [flying]), option(40, Hippogriff [walking]), option(60, Hippogriff [flying]), option(60, Pegasus [walking]), option(90, Pegasus [flying]), option(20, Peryton [walking]), option(60, Peryton [flyingg]), option(50, Unicorn), option(60, Peryton [flying]), option(50, Unicorn), option(50, Broom of Flying), option(30, Broom of Flying [over  200 lbs]), option(80, Carpet of Flying [3ft x 5ft]), option(60, Carpet of Flying [4ft x 6ft]), option(40, Carpet of Flying [5ft x 7ft]), option(30, Carpet of Flying [6ft x 9ft]), option(300, Wind Walk), option(50, Cauldron of Flying), option(30, Cart pulled by Horses), option(30, Cart pulled by PCs), option(40, PHB Galley), option(10, PHB Keelboat), option(30, PHB Longship), option(15, PHB Rowboat), option(20, PHB Sailing Ship), option(25, PHB Warship), option(50, GOS Sailing Ship), option(45, Aquisions Inc Battle Balloon), option(15, Aquisions Inc Mechanical Beholder), option(200, Ebberon Lyrandar Airship), option(100, Ebberon Lyrandar Galleon), option(300, Ebberon Orien Lightning Rail)):BaseSpeed]` |
| **Select Travel Speed:** `INPUT[inlineSelect(option(1, Normal Pace), option(1.33, Slow Pace), option(0.66, Fast Pace), showcase):SpeedMultiplier]`   |
| Additional Bonus Speed: `INPUT[number:AdditionalBonus]`  |
| Encumbered: (`VIEW[{Encumbered} ? -10: 0]`) `INPUT[toggle:Encumbered]` Horseshoes of Speed: (`VIEW[{HorseshoesofSpeed} ? 30: 0]`) `INPUT[toggle:HorseshoesofSpeed]` |
| **Travel Hours Per Day:** `INPUT[number:HoursPerDay]` |
| Exhaustion Level: `INPUT[inlineSelect(option(0, 0 No exhaustion), option(1, 1 Disadvantage on ability checks), option(2, 2 Speed halved), option(3, 3 Disadvantage on attack rolls and saving throws), option(4, 4 Hit point maximum halved), option(5, 5 Speed reduced to 0), option(6, 6 Death)):ExhaustionLevel]`  |
| New Base Speed: `VIEW[round({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus},1)]` |
| Miles To Travel:  `INPUT[number:TravelDistance]`  |
| **Days Travel 🕓:** `VIEW[round(({TravelDistance} * ({varMins}/(({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus}) / 10) * {SpeedMultiplier})) / 60 / {HoursPerDay}, 1)]`  |

##### Location Note Code
Copy the code below into another note and change the `88` to match the distance between Town A and Town B. 

`VIEW[round(145 / ({TravelConfig#TravelCalc} * {TravelConfig#HoursPerDay}), 1)]`

> [!warning]- Back End Calc
> This calculation is referenced in the travel calculation by external notes. 
> **Travel Calc:** `VIEW[((({TravelConfig#BaseSpeed} * ({TravelConfig#ExhaustionLevel} > 1 ? 2 : 1) + ({TravelConfig#Encumbered} ? -10 : 0) + ({TravelConfig#HorseshoesofSpeed} ? 30 : 0) + {TravelConfig#AdditionalBonus}) / 10) * {TravelConfig#SpeedMultiplier})][math:TravelCalc]`