# API RollOnLoot

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Rolls or passes on loot.
 RollOnLoot(rollID [, rollType])

==Arguments==
:;rollID:{{apitype|number}} - The number increases with every roll you have in a party. Maximum value is unknown.
:;rollType:{{apitype|number?}} - 0 or nil to pass, 1 to roll Need, 2 to roll Greed, or 3 to roll Disenchant.

==Example==
The code snippet below will display a message when you roll or pass on a roll. This could easily be changed to record how many times you roll on loot.
 hooksecurefunc("RollOnLoot", function(rollID, rollType)
  if (rollType and rollType > 0) then
    DEFAULT_CHAT_FRAME:AddMessage("You rolled on the item with id: " .. rollID );
  else
    DEFAULT_CHAT_FRAME:AddMessage("You passed on the item with id: " .. rollID );
  end
 end)
```