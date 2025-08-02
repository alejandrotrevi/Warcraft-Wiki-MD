# API UnitCanAssist

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Indicates whether the first unit can assist the second unit.

 canAssist = UnitCanAssist(unitToAssist, unitToBeAssisted)

==Parameters==
===Arguments===
:;unitToAssist : [[UnitId]] - the unit that would assist (e.g., "player" or "target")
:;unitToBeAssisted : [[UnitId]] - the unit that would be assisted (e.g., "player" or "target")
===Returns===
:;canAssist:{{apitype|boolean}} - 1 if the ''unitToAssist'' can assist the ''unitToBeAssisted'', nil otherwise.

==Example==
   if (UnitCanAssist("player", "target")) then 
      DEFAULT_CHAT_FRAME:AddMessage("You can assist the target.")
   else 
      DEFAULT_CHAT_FRAME:AddMessage("You cannot assist the target.")
   end
===Result===
A message indicating whether the player can assist the current target is displayed in the default chat frame.

==See also==
*{{api|UnitCanCooperate}}
```