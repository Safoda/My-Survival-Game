#♾️ALL_LISTS 
# Player Mechanics

## Player Controls


In-Game

|    Keybind ⌨️    |       Action🎬        |
| :--------------: | :-------------------: |
| LeftMouseButton  | Use item in Hand Slot |
| RightMouseButton |    Grab (and Drop)    |
|        W         |     Walk Forward      |
|        A         |       Walk Left       |
|        S         |     Walk Backward     |
|        D         |      Walk Right       |
|      Space       |         Jump          |
|      Shift       |          Run          |
|       Ctrl       |        Crouch         |
|        E         |   Equip (Hand Slot)   |
|        J         |        Journal        |
|        C         |                       |
|        M         |     Map (Journal)     |
|        B         |    Build (Journal)    |
|                  |                       |



## Physics
### Grabbing and Dropping ("RightMouseButton")

#### Objects
###### List of objects player can grab
There are objects that the player will be able to grab and carry around. These objects include:
- Food:
	- Fruits
	- Meats
	- Dead Animals
	- Drinks
- Resources:
	- Stones
	- Sticks
	- Logs
	- Leaves
	- Flowers
- Containers:
	- Baskets
	- Wheelbarrow
- Tools:
	- Weapons:
		- Spears
		- Knifes
		- Bows
		- Clubs
	- Tools:
		- Axes
		- Fishing Rod
		- Construction Hammer
		- Torches

###### List of objects player cannot grab
- Buildings
- Living Animals

##### Procedure:

- Player will be able to grab “grabbable” object if presses down "RightMouseButton".
- If player releases "RightMouseButton" and dropping mechanism is not activated (false), player will not drop object.
- If object is in hand, pressing down "RightMouseButton" will activate de dropping mechanism (true) and start a throwing bar.
- The longer "RightMouseButton" is being pressed, the more the bar fills.
- When the player releases "RightMouseButton", and dropping mechanism is true, the object will be dropped or thrown (depending on the throw bar).	

##### Object Collisions

Whenever the player grabs an object, the object will only collide with the Environment (Mask 1). And the layer will be turned off?


#### Interactable

##### Procedure:
Basically almostthe same as "objects", but Interactables cannot be thrown:

- Player will be able to grab “grabbable” object if presses down "RightMouseButton".
- If player releases "RightMouseButton" and dropping mechanism is not activated (false), player will not drop object.
- If object is in hand, pressing down "RightMouseButton" will activate de dropping mechanism (true).
- When the player releases "RightMouseButton", and dropping mechanism is true, the object will be dropped.

###### List of Interactable
- Doors
- Wheelbarrow
- Levers
- 


## Inventory System



## Player Stats
### Health
[[Health]]
### Hunger
[[Hunger]]
### Thirst
[[Thirst]]
### Fatigue(Sleeping)
[[Stamina]]
### Diseases
[[Diseases]]
### Temperature

### Weight


# Crafting


# Building
### Shelter
# Cooking
## Conserving food
**Drying**
**Smoking**
**Salting (if you have salt or seawater)**


🐟 Bonus: Preserving Fish on an Island

1. Gut it immediately
    
2. Rinse with clean seawater
    
3. Salt or brine it
    
4. Dry it in the sun or smoke it
    
5. Store in a **sealed basket or coconut husk**, away from moisture

## ❗Food to Eat Quickly (Hard to Preserve)

- Raw fruits (except bananas, coconuts)
    
- Fresh-caught shellfish (unless cooked immediately)
    
- Leafy greens
    
- Eggs (can last ~1 week in shade if unwashed

# Taming 

# Weather Mechanics

#### ideas
Hurricanes, flash floods, monsoon cycles


# Journal

📘 **Field Journal / Auto-notes** - Record discoveries: edible plants, recipes, animal tracks, star patterns

**Mystery Ingredient System** - Unknown plants must be tested or mixed — can produce surprises or disasters

Learn by experience — e.g., first contact with poison plant adds to survival journal

👣 **Memory-Based Mapping** - Map reveals only places the player remembers well — fog returns over time




# 🥲TO ORGANIZE (ideas):

**### Baskets

Baskets will allow the player to handle more items around the map:

- Player will craft baskets to be able to transport items around
- Baskets made out of rattan leaves

### Wheelbarrow

Wheelbarrow will allow the player to insert:

- Baskets (from empty to full)
- Logs
- Sticks
- Leaves



### Tool Durability






Uncover remains of past islanders, ancient ruins

🐾**Animal Tracking** - Follow footprints, broken foliage, or sounds to find prey or avoid predators

🔍 **Secret Biomes** -  Volcanic areas, glowing caves, ancient ruins, coral labyrinths

🎭 **Hallucinations & Dreams** - Nightmares, spirit animals, or memories blur reality

🧘 **Calming Actions** - Music, meditation, or painting can restore emotional balance

📝 **Journaling as Therapy** - Writing down thoughts improves clarity and may lead to gameplay insights








#### 🌱 Ecosystem Simulation Mechanics

🌳 Tree Growth & Replanting - Cutting down trees without planting new ones changes climate or causes erosion




#### ⚔️ Combat & Defense Mechanics



🪤 **Trap Crafting** - Snares, spike pits, alarms — defend base or hunt animals

🐍 **Wildlife Aggression Levels** - Animals may be defensive, predatory, or neutral depending on behavior

💀 **Permadeath / Legacy System** - If you die, your next survivor can find your old camp, journal, and gear

👥 **Tribal Conflict or Factions** (if lore allows) - Defend against or ally with other humans — adds complexity




# 🗑️Trashed Ideas

## IDEA 1 (SCRAPED)
### Interacting with objects

#### Picking objects (Tapping "E")


The idea:

Some objects are usable in the players hands, if the player taps "E" the object will snap into the Hand. 


#### Using the object in Hand 

The idea:

If the player presses "LeftClick", the object in Hand will be used.

#### Dropping object in hand

The idea:

If the player wants to drop the object in Hand, tap "g"








### Grabbing "Holding E"
A
The idea:


- 
- holding "E" for a certain amount of time will grab object
- object will snap to holding point
- player can rotate object using "R"
- releasing "E" will drop the object


## IDEA 2 (radial menu)


### Interacting with objects

#### Picking objects (Holding "E")
- When raycast detects an object, player can hold "E" to show a Radial Menu.
- This Radial Menu will have a few options depending on the object:
	- **Pick Up**
	- Consume
	- Open/Close baskets
	- Remove item from basket?
	- Etc...





#### Using the object in Hand 
After the player chooses the Pick Up option from the radial menu, the object will snap into the players Holding Point.  


#### Dropping object in hand
If the player wants to drop the object in Hand, tap "g"

### Grabbing (Holding "Left Mouse Button")
The idea:


The idea: Like the amnesia games, player can grab objects with "Left Mouse". Also open doors, levers and buttons




