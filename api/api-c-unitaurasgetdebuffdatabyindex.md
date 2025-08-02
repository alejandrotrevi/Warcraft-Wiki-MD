# API C UnitAuras.GetDebuffDataByIndex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UnitAuras|system=UnitAuras}}
Needs summary.
 aura = C_UnitAuras.GetDebuffDataByIndex(unitToken, index [, filter])

==Arguments==
:;unitToken:{{apitype|UnitToken}}
:;index:{{apitype|number}}
:;filter:{{apitype|string?}} - A list of filters, separated by pipe chars or spaces. Otherwise defaults to "HARMFUL".

==Filters==
{{:API_C_UnitAuras.GetAuraDataByIndex#Details}}
{{:AuraFilter}}

==Returns==
:;aura:{{apitype|AuraData?}}
{{:Struct AuraData|nocaption=1}}
```