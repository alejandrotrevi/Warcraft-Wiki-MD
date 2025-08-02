# API UnitPlayerControlled

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the unit is controlled by a player.
 UnitIsPlayerControlled = UnitPlayerControlled(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;UnitIsPlayerControlled:{{apitype|boolean}} - Returns true if the "unit" is controlled by a player. Returns false if the "unit" is an NPC.

==Example==

<syntaxhighlight lang="lua">
if (UnitPlayerControlled("target")) then
  DEFAULT_CHAT_FRAME:AddMessage("Your selected target is a player.",1,1,0)
else
  DEFAULT_CHAT_FRAME:AddMessage("Your selected target is an NPC.",1,1,0)
end
</syntaxhighlight>
```