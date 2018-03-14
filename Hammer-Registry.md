# HammerRegistry.json
This is the registry for hammering Blocks into a different Item, mostly used for Cobble -> Gravel -> Sand -> Dust.

## Syntax
The syntax is one large Map (Therefore enclosed by `{ ... }`) followed by many comma separated entries which each have a list of items they can drop (`"key": [{...}, {...}, ...]`) for the different items.

### Example
```json
{
  "minecraft:concrete:8": [
    {
      "item": "minecraft:concrete_powder:8",
      "amount": 1,
      "miningLevel": 1,
      "chance": 1.0,
      "fortuneChance": 0.0
    }
  ],
  "ore:sand": [
    {
      "item": "exnihilocreatio:block_dust:0",
      "amount": 1,
      "miningLevel": 0,
      "chance": 1.0,
      "fortuneChance": 0.0
    }
  ]
}
```

## Explanation:
* `"key": [....]`:  
  The key can be two things here:
  1. **Item**:
    `"modid:item:meta"` (for example: `"minecraft:concrete:8"`)
  2. **OreDict**:
    `ore:ORENAME` (for example `"ore:sand"`)

* `"amount": 1`:  
  The amount that should drop when breaking the block with a hammer

* `"miningLevel": 1`:  
  Mininglevel which is needed to break this block.
  `(3 = DIAMOND, 2 = IRON, 1 = STONE, 0 = WOOD/GOLD)`

* `"chance": 1.0`:  
  The drop at which it should drop when broken with a normal tool

* `"fortuneChance": 0.0`:  
  How much the drop rate should increase when the tool has a fortune effect on it.
