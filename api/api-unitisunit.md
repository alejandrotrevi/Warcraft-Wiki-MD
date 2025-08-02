# API UnitIsUnit

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the specified units are the same unit.
 isSame = UnitIsUnit(unit1, unit2)

==Arguments==
:;unit1:{{apitype|string}} : [[UnitId]] - The first unit to query (e.g. "party1", "pet", "player")
:;unit2:{{apitype|string}} : [[UnitId]] - The second unit to compare it to (e.g. "target")

==Returns==
:;isSame:{{apitype|boolean}} - 1 if the two units are the same entity, nil otherwise.

==Example==
 if ( UnitIsUnit("targettarget", "player") ) then
  message("Look at me, I have aggro from " .. UnitName("target") .. "!");
 end;
===Result===
Displays a message if your target is targetting you.
```