# API C UnitAuras.IsAuraFilteredOutByInstanceID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Tests if an aura passes a specific filter.
 isFiltered = C_UnitAuras.IsAuraFilteredOutByInstanceID(unit, auraInstanceID, filterString)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to query.
:;auraInstanceID:{{apitype|number}} - The aura instance ID to test.
:;filterString:{{apitype|string}} - The aura filter string to test, eg. "HELPFUL" or "HARMFUL".

==Filters==
{{:AuraFilter}}

==Returns==
:;isFiltered:{{apitype|boolean}} - <code>true</code> if the aura passes the specified filter, or <code>false</code> if not.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```