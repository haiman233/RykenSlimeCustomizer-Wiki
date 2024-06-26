# 物品

**示例：**
```yaml
EXAMPLE_ITEM:
  item_group: example_sub_group
  placeable: false
  item:
    name: "&a示例物品"
    material: DIAMOND
    amount: 1
  recipe_type: ENHANCED_CRAFTING_TABLE  
  recipe:
    1:
      material: APPLE
      amount: 1
  radiation: HIGH
EXAMPLE_ITEM_2:
  item_group: example_normal_group
  placeable: false
  item:
    name: "&a示例物品2"
    material: NETHERITE_INGOT
    amount: 1
  recipe_type: ENHANCED_CRAFTING_TABLE  
  script: "example_item_2"
  recipe:
    1:
      material_type: slimefun
      material: EXAMPLE_ITEM
      amount: 1
  energy_capacity: 100
```
| 内容 | 描述 | 有效输入 |
| --- | ----------- | ----------------- |
| `EXAMPLE_ITEM` | 物品的ID。<br>该ID不能与任何其他物品的ID相同! | **仅支持大写字母、数字、下划线!** |
| item_group | 物品所在[物品组（分类）](groups.md)的ID。 |
| item.# | [通用物品格式](../format/universal-item-format.md)| 可选择性添加modelId、lore、glow等 |
| placeable | 物品是否可放置。**不要让工具等本来就无法放置的物品可放置！** |
| recipe_type | 见 SlimeCustomizer wiki[合成配方](https://slimefun-addons-wiki.guizhanss.cn/slime-customizer/Crafting-Recipe) ，可填自定义的recipe_type详见[配方类型](recipe_type.md)。 |
| script | 物品引用的脚本，设置物品对应的脚本文件，双引号内填脚本对应的文件名称 |
| recipe | 设置物品的配方。详见[**配方**](../format/recipe.md) |
| energy_capacity | 可充电物品的充电量，详见下文 |
| radiation | 辐射等级，详见下文 |
| rainbow | 彩虹方块，详见下文 |
| rainbow_materials | 自定义彩虹方块，详见下文 |
| anti_wither | 防凋灵，详见下文 |
| soulbound | 灵魂绑定，详见下文 |
| piglin_trade.piglin_chance | 猪灵交易物品，详见下文 |
| vanilla | 人造类物品，详见下文 |

### 可充电物品

```
energy_capacity: <容量>
```

容量最大为 2147483647 。

*提示：仅通过添加energy_capacity的可充电物品是没有任何功能的，如果想让可充电物品拥有其它功能，需要搭配脚本使用*

### 辐射

```
 radiation: <辐射等级>
```

辐射等级详见[辐射](https://slimefun.github.io/javadocs/Slimefun4/docs/io/github/thebusybiscuit/slimefun4/core/attributes/Radioactivity.html)

### 彩虹方块与自定义彩虹方块

```
 rainbow: <类型>
```

彩虹方块类型包括：GLASS_PANE（玻璃板）、GLASS（玻璃）、STAINED_GLASS（彩色玻璃）、STAINED_GLASS_PANE（彩色玻璃板）、WOOL（羊毛）、 TERRACOTTA（陶瓦）、TERRACOTTA_ALL（所有陶瓦）、GLAZED_TERRACOTTA（带釉陶瓦）

```
 rainbow_materials:
    - GRASS_BLOCK
    - DIRT
```

自定义彩虹方块，按照上述格式添加方块ID

### 防凋灵

```
 anti_wither: true/false
```

注意：只有方块可以设置这个选项
当anti_wither为true时，该方块将无法被凋灵破坏

### 灵魂绑定

```
 soulbound: true
```

当soulbound为true时，该物品将不会在玩家死亡后掉落

### 猪灵交易物品

```
 piglin_trade:
     piglin_trade_chance: <0-100>
```

设置此物品的获取方式为猪灵交易物品，记得改recipe_type

### 人造类物品

```
 vanilla: true/false
```

类似于人造钻石，当vanilla为true时，此物品可以被当做原版物品作为原版工作台合成物品时的材料

## 注意事项

关于item.#后的标签，本页仅以name、material、amount为示例，可以在amount后添加更多标签，详见[通用物品格式](../format/universal-item-format.md)

注意name与material为必填，如果不填material_type，则默认检测material为原版物品

### 关于本页引用的示例脚本example_item_2
详见[脚本基础-物品](../scripts-basic/items.md)
