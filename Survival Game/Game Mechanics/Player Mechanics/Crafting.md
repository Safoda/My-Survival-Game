
# Ways to craft



## Recipes 

#####







# From ChatGPT

Creating a **crafting system in Godot 4** that allows you to **easily add new recipes** is best done using **Resources**, **dictionaries**, and optionally **JSON or external data**.

Here’s a clean, modular way to set it up:

---

## 🧱 STEP-BY-STEP CRAFTING SYSTEM (Godot 4)

---

### 📁 1. **Define a `CraftingRecipe` Resource**

Create a custom `.gd` resource script:

#### `CraftingRecipe.gd`

```gdscript
extends Resource
class_name CraftingRecipe
@icon("res://icon.svg") # Optional: assign an icon in the editor

@export var name: String
@export var ingredients: Dictionary  # { "wood": 3, "stone": 1 }
@export var result_item: String
@export var result_amount: int = 1
```

✅ This allows you to create new `.tres` resource files for each recipe in the Godot editor.

---

### 🧪 2. **Example Recipes (`.tres` Files)**

Create a folder like `res://Crafting/Recipes/`.

Create a `stone_axe.tres`:

```plaintext
name: "Stone Axe"
ingredients: { "wood": 2, "stone": 1 }
result_item: "stone_axe"
result_amount: 1
```

You can now **add new recipes by duplicating and editing `.tres` files** — no code changes needed.

---

### 🧠 3. **Inventory System**

Assume you have an `Inventory` script (dict-based):

#### Example:

```gdscript
var items: Dictionary = {
    "wood": 5,
    "stone": 2,
    "iron": 0
}
```

---

### 🛠 4. **Crafting Manager**

Create a `CraftingManager.gd` that handles checking and crafting:

```gdscript
extends Node

@export var recipes: Array[CraftingRecipe]  # Drag and drop `.tres` files in editor
var inventory: Dictionary = {}

func set_inventory(inv: Dictionary):
    inventory = inv

func can_craft(recipe: CraftingRecipe) -> bool:
    for ingredient in recipe.ingredients:
        if inventory.get(ingredient, 0) < recipe.ingredients[ingredient]:
            return false
    return true

func craft(recipe: CraftingRecipe) -> bool:
    if not can_craft(recipe):
        return false

    # Remove ingredients
    for ingredient in recipe.ingredients:
        inventory[ingredient] -= recipe.ingredients[ingredient]

    # Add crafted item
    inventory[recipe.result_item] = inventory.get(recipe.result_item, 0) + recipe.result_amount

    return true
```

---

### 🧩 5. **Usage Example**

```gdscript
var manager = $CraftingManager
manager.set_inventory(player_inventory)

for recipe in manager.recipes:
    if manager.can_craft(recipe):
        manager.craft(recipe)
```

---

## 🧱 Why This Works Well

|Feature|Benefit|
|---|---|
|`Resource`-based recipes|Easy to add new ones in editor|
|Dictionary ingredients|Flexible & extendable|
|Clean separation|UI, logic, and data decoupled|
|Supports JSON or .tres|You can load recipes from files|

---

## 🧪 Optional: Load Recipes from JSON (Instead of `.tres`)

If you prefer a modding-friendly format:

### `recipes.json`

```json
[
  {
    "name": "Stone Pickaxe",
    "ingredients": { "wood": 2, "stone": 3 },
    "result_item": "stone_pickaxe",
    "result_amount": 1
  }
]
```

### Load in GDScript:

```gdscript
var recipe_data = load("res://recipes.json").get_as_text()
var raw_recipes = JSON.parse_string(recipe_data)

for recipe_dict in raw_recipes:
    var recipe = CraftingRecipe.new()
    recipe.name = recipe_dict["name"]
    recipe.ingredients = recipe_dict["ingredients"]
    recipe.result_item = recipe_dict["result_item"]
    recipe.result_amount = recipe_dict["result_amount"]
    recipes.append(recipe)
```

---

Would you like a working example project or how to connect this to a UI for drag-and-drop crafting?
