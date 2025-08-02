# API C Item.GetItemQuality

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Needs summary.
 itemQuality = C_Item.GetItemQuality(itemLocation)
             = C_Item.GetItemQualityByID(itemInfo)

==Arguments==
===<font color="#4ec9b0">GetItemQuality</font>===
:;itemLocation:{{apitype|ItemLocationMixin}}
===<font color="#4ec9b0">GetItemQualityByID</font>===
:;itemInfo:{{apitype|number,string}} : {{:ItemInfo}}

==Returns==
:;itemQuality:{{apitype|Enum.ItemQuality?}}
{{:Enum.ItemQuality|nocaption=1}}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|GetItemQualityColor}}()
```