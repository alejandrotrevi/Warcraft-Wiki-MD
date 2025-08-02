# API C UnitAuras.GetAuraDataByIndex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UnitAuras|system=UnitAuras}}
Needs summary.
 aura = C_UnitAuras.GetAuraDataByIndex(unitToken, index [, filter])

==Arguments==
:;unitToken:{{apitype|UnitToken}}
:;index:{{apitype|number}}
:;filter:{{apitype|string?}} - A list of filters, separated by pipe chars or spaces. Otherwise defaults to "HELPFUL".

==Filters==
<onlyinclude>* {{api|C_UnitAuras.GetBuffDataByIndex}} is an alias for <code>{{api|C_UnitAuras.GetAuraDataByIndex}}(unit, index, "HELPFUL")</code>, returning only buffs and ignores any HARMFUL filter.
* {{api|C_UnitAuras.GetDebuffDataByIndex}} is an alias for <code>{{api|C_UnitAuras.GetAuraDataByIndex}}(unit, index, "HARMFUL")</code>, returning only debuffs and ignores any HELPFUL filter.</onlyinclude>
{{:AuraFilter}}

==Returns==
:;aura:{{apitype|AuraData?}}
{{:Struct AuraData|nocaption=1}}
```