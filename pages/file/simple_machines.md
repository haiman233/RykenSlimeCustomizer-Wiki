# 简单机器

```yaml
EX_ADVANCED_GOLD_PAN:
  item_group: example_sub_group
  item:
    material: FURNACE
    name: "&b&l超级&7淘金机"
    lore:
      - "&7一个更加快的淘金机"
      - ""
      - "&8⇨ &e⚡ &7速度: 50x"
      - "&8⇨ &e⚡ &71,000 J/s"
  type: ELECTRIC_SMELTERY
  settings:
    capacity: 5000
    consumption: 1000
    speed: 50
  recipe_type: ENHANCED_CRAFTING_TABLE
  recipe:
    2:
      material_type: full_slimefun
      material: GOLD_PAN
    4:
      material_type: full_slimefun
      material: ELECTRIC_MOTOR
    5:
      material_type: full_slimefun
      material: ELECTRIC_GOLD_PAN_3
    6:
      material_type: full_slimefun
      material: ELECTRIC_MOTOR
    7:
      material_type: full_slimefun
      material: COBALT_INGOT
    8:
      material_type: full_slimefun
      material: BLISTERING_INGOT_3
    9:
      material_type: full_slimefun
      material: COBALT_INGOT
```

| 内容 | 描述 | 有效输入 |
| --- | ----------- | ----------------- |
| `EX_ADVANCED_GOLD_PAN` | 机器的ID。<br>该ID不能与任何其他物品的ID相同! | **仅支持大写字母、数字、下划线!** |
| item_group | 物品所在[物品组（分类）](file/groups.md)的ID。 |
| item.# | [通用物品格式](format/universal-item-format.md)| 可选择性添加modelId、lore、glow等。 |
| type | 简单机器类型，详见注意事项。 |
| settings.capacity | 设置机器可储存的能量，最大为 2147483647。 |
| settings.consumption | 机器运行消耗的能量，最大为 2147483647。 |
| settings.speed | 机器运行速度，最大为 2147483647，数值越大，机器运行的越快。 |
| recipe_type | 见 SlimeCustomizer wiki[合成配方](https://slimefun-addons-wiki.guizhanss.cn/slime-customizer/Crafting-Recipe) ，可填自定义的recipe_type详见[配方类型](file/recipe_type.md)。 |
| recipe | 设置机器的配方。详见[**配方**](../format/recipe.md) |

## 注意事项
1、关于简单机器类型(type)

简单机器类型仅包含以下几种：

    ELECTRIC_SMELTERY 电动冶炼炉  
    ELECTRIC_FURNACE 电炉  
    ELECTRIC_GOLD_PAN 电动淘金机 
    ELECTRIC_DUST_WASHER 电动洗矿机  
    ELECTRIC_ORE_GRINDER 电动碎矿机  
    ELECTRIC_INGOT_FACTORY 电动铸锭机  
    ELECTRIC_INGOT_PULVERIZER 电动打粉机  
    CHARGING_BENCH 充电台 
    TREE_GROWTH_ACCELERATOR 树木生长加速器
	ANIMAL_GROWTH_ACCELERATOR 动物生长加速器
	CROP_GROWTH_ACCELERATOR 作物生长加速器
