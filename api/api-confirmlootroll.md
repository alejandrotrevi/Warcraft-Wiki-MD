# API ConfirmLootRoll

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Confirms a loot roll.
 ConfirmLootRoll(rollID[ ,roll])

==Arguments==
:;rollID:{{apitype|number}} - As passed by the event. (The number increases with every roll you have in a party)
:;roll:{{apitype|number}} - Type of roll: (also passed by the event)
::1 : Need roll
::2 : Greed roll
::3 : Disenchant roll

==Example==
 local f = CreateFrame("Frame", "MyAddon")
 f:RegisterEvent("CONFIRM_LOOT_ROLL")
 f:SetScript("OnEvent",function(self,event,...)
   if event == "CONFIRM_LOOT_ROLL" then
     local rollID, roll = ...
     ConfirmLootRoll( rollID, roll )
   end   
 end)

==See also==
* {{api|t=e|CONFIRM_LOOT_ROLL}}
* {{api|t=e|CONFIRM_DISENCHANT_ROLL}}
```