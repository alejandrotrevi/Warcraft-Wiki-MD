# API C GameRules.GetGameRuleAsFloat

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GameRules|system=GameRules}}
Returns the numeric value specified in the Game Rule, multiplied by 0.1 for every decimal place requested
 value = C_GameRules.GetGameRuleAsFloat(gameRule [, decimalPlaces])

==Arguments==
:;gameRule:{{apitype|Enum.GameRule}}
:;decimalPlaces:{{apitype|number?|default=0}}

{{:Enum.GameRule}}

==Returns==
:;value:{{apitype|number}}
```