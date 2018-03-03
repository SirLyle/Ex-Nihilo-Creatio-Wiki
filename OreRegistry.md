# OreRegistry.json

This is for Registering the different chunks, pieces, dusts and ingots.

##  Syntax
The syntax is one large Array (Therefore enclosed by `[ ... ]`) followed by many comma separated blocks (`{...}`) for the different ores.

#### Example:
```json
[
  {
    "name": "gold",
    "color": {
      "r": 1.0,
      "g": 1.0,
      "b": 0.0,
      "a": 1.0
    },
    "result": {
      "name": "minecraft:gold_ingot",
      "meta": 0
    },
    "oredictName": "TotalyNotGold",
    "translations": {
      "de_de": "THISISGOLD!",
      "zh_cn": "金"
    }
  },
  {
    "name": "iron",
    "color": {
      "r": 0.7490196,
      "g": 0.5019608,
      "b": 0.2509804,
      "a": 1.0
    },
    "result": {
      "name": "minecraft:iron_ingot",
      "meta": 0
    }
  }
]
```


### Explation:
* `"name": "NAME"`:  
The registry name the item will get
* `"color": { ... }`:  
The rgb color the item will have, in this context alpha is irrelevant
* `"result": { ... }`: _(Optional)_  
The ingot that is attached to the Ore, if none is provided the mod will create a ingot on it's own
* `"oredictName": "ORENAME"`: _(Optional)_  
The oreDict name the Item will get, this is appended to the _Base Names_ configured in the main config, will use Registry name if not provided
* `"translations": { "lang_key": "translation", ...}`: _(Optional)_  
A Map of different translations for different languages, will use Registry name if not provided