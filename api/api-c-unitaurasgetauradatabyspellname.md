# API C UnitAuras.GetAuraDataBySpellName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UnitAuras|system=UnitAuras}}
Needs summary.
 aura = C_UnitAuras.GetAuraDataBySpellName(unitToken, spellName [, filter])

==Arguments==
:;unitToken:{{apitype|string}} - [[UnitId]]
:;spellName:{{apitype|string}}
:;filter:{{apitype|string?}} - A list of filters, separated by pipe chars or spaces. Otherwise defaults to "HELPFUL".

==Filters==
{{:AuraFilter}}

==Returns==
:;aura:{{apitype|AuraData?}}
{{:Struct AuraData|nocaption=1}}
```