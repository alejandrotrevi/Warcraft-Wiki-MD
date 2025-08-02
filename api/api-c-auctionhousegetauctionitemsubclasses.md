# API C AuctionHouse.GetAuctionItemSubClasses

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Needs summary.
 subClasses = C_AuctionHouse.GetAuctionItemSubClasses(classID)

==Arguments==
:;classID:{{apitype|number}} - Item [[ItemType#Item_Type|classID]]

==Returns==
:;subClasses:{{apitype|number[]}}

==Example==
Prints all subclass IDs for the Consumables category.
<syntaxhighlight lang="lua">
local classID = LE_ITEM_CLASS_CONSUMABLE
for _, subClassID in pairs(C_AuctionHouse.GetAuctionItemSubClasses(classID)) do
	print(subClassID, (GetItemSubClassInfo(classID, subClassID)))
end
</syntaxhighlight>

 0, Explosives and Devices
 1, Potion
 2, Elixir
 3, Flask
 5, Food & Drink
 7, Bandage
 9, Vantus Runes
 8, Other

==Values==
{| class="sortable darktable zebra"
! Enum !! classID !! subClasses
|-
| LE_ITEM_CLASS_CONSUMABLE || <center>0</center> || {0, 1, 2, 3, 5, 7, 9, 8}
|-
| LE_ITEM_CLASS_CONTAINER || <center>1</center> || {0, 2, 3, 4, 5, 6, 7, 8, 9, 10}
|-
| LE_ITEM_CLASS_WEAPON || <center>2</center> || {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 13, 14, 15, 16, 18, 19, 20}
|-
| LE_ITEM_CLASS_GEM || <center>3</center> || {11, 0, 1, 2, 3, 5, 6, 7, 8, 9, 10}
|-
| LE_ITEM_CLASS_ARMOR || <center>4</center> || {0, 1, 2, 3, 4, 5, 6}
|-
| LE_ITEM_CLASS_REAGENT || <center>5</center> || {0, 1}
|-
| LE_ITEM_CLASS_PROJECTILE || <center>6</center> || {}
|-
| LE_ITEM_CLASS_TRADEGOODS || <center>7</center> || {5, 6, 7, 8, 9, 12, 16, 4, 1, 10, 11}
|-
| LE_ITEM_CLASS_ITEM_ENHANCEMENT || <center>8</center> || {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14}
|-
| LE_ITEM_CLASS_RECIPE || <center>9</center> || {0, 1, 2, 3, 4, 6, 8, 10, 11, 5, 7, 9}
|-
| (Money) || <center>10</center> || {0}
|-
| LE_ITEM_CLASS_QUIVER || <center>11</center> || {}
|-
| LE_ITEM_CLASS_QUESTITEM || <center>12</center> || {0}
|-
| LE_ITEM_CLASS_KEY || <center>13</center> || {0, 1}
|-
| (Permanent) || <center>14</center> || {0}
|-
| LE_ITEM_CLASS_MISCELLANEOUS || <center>15</center> || {0, 1, 2, 3, 5, 6, 4}
|-
| LE_ITEM_CLASS_GLYPH || <center>16</center> || {1, 2, 3, 4, 5, 7, 8, 9, 11, 6, 10, 12}
|-
| LE_ITEM_CLASS_BATTLEPET || <center>17</center> || {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
|-
| LE_ITEM_CLASS_WOW_TOKEN || <center>18</center> || {0}
|}

==Patch changes==
* {{Patch 8.3.0|note=Added, replaces {{api|GetAuctionItemSubClasses}}()}}

==See also==
* {{api|GetItemClassInfo}}()
* {{api|GetItemSubClassInfo}}()

{{apinavbox|C_AuctionHouse}}
```