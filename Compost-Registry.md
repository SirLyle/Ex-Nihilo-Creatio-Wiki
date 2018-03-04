# CompostRegistry.json
This is the registry for composting Items in the barrel into a different Block, mostly dirt.

## Syntax
The syntax is one large Map (Therefore enclosed by `{ ... }`) followed by many comma separated entries (`"key": {...}`) for the different items.

### Example
```json
{
  "ore:treeLeaves": {
    "value": 0.125,
    "compostBlock": "minecraft:dirt:0"
  },
  "minecraft:melon:0": {
    "value": 0.04,
    "compostBlock": "minecraft:dirt:0",
    "color": "ff443b"
  }
}
```

## Explanation:
* `"key": {....}`:  
  The key can be two things here:
  1. **Item**:
    `"modid:item:meta"` (for example: `"minecraft:melon:0"`)
  2. **OreDict**:
    `ore:ORENAME` (for example `"ore:treeLeaves"`)

* `"value": 0.125`:  
  The amount it should **progress toward the full block**, 1 is the full block, therefore it would need 8 items with 0.125

* `"color": "ff443b"`: _(Optional)_  
  This **defines the color** the item will have inside the barrel  
  This can be **left away** (for oredicts for example) and then it will automatically chose a color of the item that has been 
  put in. [!! This needs **JEI to be installed on the client** !!]
