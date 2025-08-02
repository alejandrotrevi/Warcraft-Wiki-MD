# API UnitIsPVP

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the unit is flagged for PVP.
 ispvp = UnitIsPVP(unit)

----
;''Arguments''

:;unit ([[API_TYPE_UnitId|UnitID]]):the unit name (e.g., "target")

----
;''Returns''

:;ispvp:1 if the unit is flagged for PvP, nil otherwise.

----
;''Example''

 if (UnitIsPVP("target")) then
  -- Target is flagged for PvP
 end
```