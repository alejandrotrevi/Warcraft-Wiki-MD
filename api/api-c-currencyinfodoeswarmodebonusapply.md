# API C CurrencyInfo.DoesWarModeBonusApply

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_CurrencyInfo|system=CurrencySystem}}
Needs summary.
 warModeApplies, limitOncePerTooltip = C_CurrencyInfo.DoesWarModeBonusApply(currencyID)

==Arguments==
:;currencyID:{{apitype|number}} : [[CurrencyID]]

==Returns==
:;warModeApplies:{{apitype|boolean?}}
:;limitOncePerTooltip:{{apitype|boolean?}}

==Patch changes==
* {{Patch 8.2.0|note=Added <code>limitOncePerTooltip</code> return.}}
* {{Patch 8.1.0|note=Added.}}
```