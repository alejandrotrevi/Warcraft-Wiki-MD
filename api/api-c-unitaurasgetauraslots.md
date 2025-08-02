# API C UnitAuras.GetAuraSlots

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_UnitAuras|system=UnitAuras}}
Needs summary.
 outContinuationToken, slots, ... = C_UnitAuras.GetAuraSlots(unitToken [, filter [, maxSlots [, continuationToken]]])

==Arguments==
:;unitToken:{{apitype|UnitToken}}
:;filter:{{apitype|string?}}
:;maxSlots:{{apitype|number?}}
:;continuationToken:{{apitype|number?}}

==Returns==
:;outContinuationToken:{{apitype|number?}}
(Variable returns)
:;slots:{{apitype|number}}
```