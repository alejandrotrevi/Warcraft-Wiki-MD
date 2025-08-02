# API C AuctionHouse.GetItemKeyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AuctionHouse|system=AuctionHouse}}
Returns more details about an item from its item key, including its name.
 itemKeyInfo = C_AuctionHouse.GetItemKeyInfo(itemKey [, restrictQualityToFilter])

==Arguments==
:;itemKey:{{apitype|ItemKey}}
{{:Struct ItemKey|nocaption=1}}
:;restrictQualityToFilter:{{apitype|boolean?|default=false}}

==Returns==
:;itemKeyInfo:{{apitype|ItemKeyInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| itemID || {{apitype|number}} || <font color="green">9.2.7</font>
|-
| battlePetSpeciesID || {{apitype|number}} || <font color="green">9.2.7</font>
|-
| itemName || {{apitype|string}} || 
|-
| battlePetLink || {{apitype|string?}} || 
|-
| appearanceLink || {{apitype|string?}} || 
|-
| quality || {{apitype|Enum.ItemQuality}} || 
|-
| iconFileID || {{apitype|number}} || 
|-
| isPet || {{apitype|boolean}} || 
|-
| isCommodity || {{apitype|boolean}} || 
|-
| isEquipment || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Hotfix|date=2020-02-27|version=33528|note=Added appearanceLink return value<ref>{{Ref FrameXML|Blizzard_APIDocumentation/AuctionHouseDocumentation.lua|8.3.0|33528|1316|2020-02-27}}</ref>|doc=}}
* {{Patch 8.3.0|note=Added.}}

==References==
{{Reflist}}

{{apinavbox|C_AuctionHouse}}
```