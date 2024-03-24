---
obsidianUIMode: preview
obsidianEditingMode: source
BaseSpeed: 30
SpeedMultiplier: 1
AdditionalBonus: 0
Encumbered: false
HorseshoesofSpeed: false
HoursPerDay: 8
MinutesPerMile: 20
ExhaustionLevel: 0
TravelDistance: 88
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
TravelCalc: 20
---

# Travel Speed
Updating the calculator below will flows the changes out to any notes that automatically calculate the travel distance. You need to refresh this note in order to see calculated changes. 

![[Traveling Party.jpg|right|300]]

| DnD5e Travel Calculator | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Select Base Speed:** `INPUT[inlineSelect(option(30.001, Walking), option(50.001, Camel), option(40.001, Donkey), option(40.002, Mule), option(40.003, Draft Horse), option(40.004, Elephant), option(40.005, Mastiff), option(40.006, Moorbounder), option(40.007, Pony), option(40.008, Rhinoceros), option(60.001, Riding Horse), option(40.009, Saber-Toothed Tiger), option(60.002, Warhorse), option(20.001, Griffon [walking]), option(80.001, Griffon [flying]), option(40.010, Hippogriff [walking]), option(60.003, Hippogriff [flying]), option(60.004, Pegasus [walking]), option(90.001, Pegasus [flying]), option(20.002, Peryton [walking]), option(60.005, Peryton [flyingg]), option(50.002, Unicorn), option(60.006, Peryton [flying]), option(50.003, Unicorn), option(50.004, Broom of Flying), option(30.002, Broom of Flying [over  200 lbs]), option(80.002, Carpet of Flying [3ft x 5ft]), option(60.007, Carpet of Flying [4ft x 6ft]), option(40.011, Carpet of Flying [5ft x 7ft]), option(30.003, Carpet of Flying [6ft x 9ft]), option(300.001, Wind Walk), option(50.005, Cauldron of Flying), option(30.004, Cart pulled by Horses), option(30.005, Cart pulled by PCs), option(40.012, PHB Galley), option(10.001, PHB Keelboat), option(30.006, PHB Longship), option(15.001, PHB Rowboat), option(20.003, PHB Sailing Ship), option(25.001, PHB Warship), option(50.006, GOS Sailing Ship), option(45.001, Aquisions Inc Battle Balloon), option(15.003, Aquisions Inc Mechanical Beholder), option(200.001, Ebberon Lyrandar Airship), option(100.001, Ebberon Lyrandar Galleon), option(300.002, Ebberon Orien Lightning Rail)):BaseSpeed]` |
| **Select Travel Speed:** `INPUT[inlineSelect(option(1, Normal Pace), option(1.333333, Slow Pace), option(0.666667, Fast Pace), showcase):SpeedMultiplier]`   |
| Additional Bonus Speed: `INPUT[number:AdditionalBonus]`  |
| Encumbered: `INPUT[toggle:Encumbered]` (`VIEW[{Encumbered} ? -10: 0]`) Horseshoes of Speed: `INPUT[toggle:HorseshoesofSpeed]` (`VIEW[{HorseshoesofSpeed} ? 30: 0]`)  |
| **Travel Hours Per Day:** `INPUT[number:HoursPerDay]` |
| Exhaustion Level: `INPUT[inlineSelect(option(0, 0 No exhaustion), option(1, 1 Disadvantage on ability checks), option(2, 2 Speed halved), option(3, 3 Disadvantage on attack rolls and saving throws), option(4, 4 Hit point maximum halved), option(5, 5 Speed reduced to 0), option(6, 6 Death)):ExhaustionLevel]`  |
| New Base Speed: `VIEW[round({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus},1)]` |
| Miles To Travel:  `INPUT[number:TravelDistance]`  |
| **Days Travel 🕓:** `VIEW[round(({TravelDistance} * ({varMins}/(({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus}) / 10) * {SpeedMultiplier})) / 60 / {HoursPerDay}, 1)]`  |

### Travelling More Than 8 Hours A Day
Requires hourly [[08-using-ability-scores#Constitution Checks|Constitution Saves]]  after 8 hours:

DC 11 at hour 9
DC 12 at hour 10
Each failure adds a level of [[conditions#Exhaustion|Exhaustion]].

### Transport Services

|                     |                                                                                                                                        |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **Danger Level:**   | `INPUT[inlineSelect(option(1.5, Safe Route), option(2, Chance of Bandits), option(3, Hostile Lands), option(5, Warzone)):DangerLevel]` |
| **Familiar Route:** | `INPUT[toggle:FamiliarRoute]`                                                                                                          |
| **Party Members:** | `INPUT[number:PartyMembers]`                                                                                                           |
| **Lifestyle:**   | `INPUT[inlineSelect(option(0, Wretched), option(1, Squalid), option(2, Poor), option(10, Modest), option(20, Comfortable), option(40, Wealthy), option(100, Aristocratic)):LifestyleCostSP]` |
| **Include Meals:** | `INPUT[toggle:IncludeMeals]` `VIEW[round(({IncludeMeals} ? 1 : 0)*(({LifestyleCostSP}/10)*{PartyMembers})*round(({TravelDistance} * ({varMins}/(({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus}) / 10) * {SpeedMultiplier})) / 60 / {HoursPerDay}),1)]`gp.                                                                                                          |
<br>

| Service               | Cost Per Mile (cp.)                     | Total Cost gp.cp |
| --------------------- | --------------------------------- | ---------- |
| Coach (between towns) | `INPUT[number:CoachCostPerM]`     | `VIEW[round({TravelDistance}*({CoachCostPerM}*({DangerLevel}+({FamiliarRoute} ? -0.5 : 0))*{PartyMembers}),0)/100+(({IncludeMeals} ? 1 : 0)*(({LifestyleCostSP}/10)*{PartyMembers})*round(({TravelDistance} * ({varMins}/(({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus}) / 10) * {SpeedMultiplier})) / 60 / {HoursPerDay}))]`gp.            |
| Coach (within city)   | `INPUT[number:CoachCost]`         | `VIEW[round(({CoachCost}*({DangerLevel}+({FamiliarRoute} ? -0.5 : 0))*{PartyMembers}),0)/100]`gp.          |
| Send Messenger        | `INPUT[number:MessengerCostPerM]` | `VIEW[round({TravelDistance}*({MessengerCostPerM}*({DangerLevel}+({FamiliarRoute} ? -0.5 : 0))),0)/100]`gp.           |
| Ships Passage         | `INPUT[number:ShipCostPerM]`      | `VIEW[round({TravelDistance}*({ShipCostPerM}*({DangerLevel}+({FamiliarRoute} ? -0.5 : 0))*{PartyMembers}),0)/100+(({IncludeMeals} ? 1 : 0)*(({LifestyleCostSP}/10)*{PartyMembers})*round(({TravelDistance} * ({varMins}/(({BaseSpeed} / ({ExhaustionLevel} > 1 ? 2 : 1) + ({Encumbered} ? -10 : 0) + ({HorseshoesofSpeed} ? 30 : 0) + {AdditionalBonus}) / 10) * {SpeedMultiplier})) / 60 / {HoursPerDay}))]`gp.           |

##### Location Note Code
Copy the code below into another note and change the `88` to match the distance between Town A and Town B. 

`VIEW[round((88* {TravelCalculator#TravelCalc}) / 60 / {TravelCalculator#HoursPerDay}, 1)]`

> [!warning]- Back End Calc
> This calculation is referenced in the travel calculation by external notes. 
> **Travel Calc:** `VIEW[({TravelCalculator#varMins}/(({TravelCalculator#BaseSpeed} / ({TravelCalculator#ExhaustionLevel} > 1 ? 2 : 1) + ({TravelCalculator#Encumbered} ? -10 : 0) + ({TravelCalculator#HorseshoesofSpeed} ? 30 : 0) + {TravelCalculator#AdditionalBonus}) / 10) * {TravelCalculator#SpeedMultiplier})][math:TravelCalc]`