# API UnitIsAFK

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns true if a friendly unit is AFK (Away from keyboard).
 isAFK = UnitIsAFK(unit)

===Arguments===
:;unit:The [[UnitId]] to return AFK status of. A nil value throws an error.

===Returns===
:; isAFK:{{apitype|boolean}} true if unit is AFK, Boolean false otherwise. An invalid or nonexistent unit value also returns false.

==Example==
If the player is AFK, the following script outputs "You are AFK" to the default chat window.
 if UnitIsAFK("player") then
   DEFAULT_CHAT_FRAME:AddMessage("You are AFK");
 end

===History===
Up until the WOD beta, the return value isAFK used to be 1 instead of true, and nil instead of false.
```