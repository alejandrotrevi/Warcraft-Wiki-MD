# API UnitIsDND

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns true if a unit is DND (Do not disturb).
 isDND = UnitIsDND(unit)

===Arguments===
:;unit:The [[UnitId]] to return DND status of.

===Returns===
:;isDND:1 if unit is DND, nil otherwise.

==Example==
If the player is DND, the following script outputs "You are DND" to the default chat window.
 if UnitIsDND("player") then
   DEFAULT_CHAT_FRAME:AddMessage("You are DND");
 end
```