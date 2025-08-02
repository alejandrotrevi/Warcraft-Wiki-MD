# API GetEclipseDirection

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Indicates which [[Eclipse]] state the player is moving towards.
 direction = GetEclipseDirection()

==Returns==

:;direction
:: String - which Eclipse state the player is moving towards:
::* "moon"
::* "sun"
::* "none"

==Example==

 local direction = GetEclipseDirection()
 if direction == "moon" then
     DEFAULT_CHAT_FRAME:AddMessage("Cast Nature spells to move toward a Lunar eclipse!")
 elseif direction == "sun" then
     DEFAULT_CHAT_FRAME:AddMessage("Cast Arcane spells to move toward a Solar eclipse!")
 end

===Result===

Adds a message to the chat frame telling the player which type of spells will move them closer to their next Eclipse state.

==Details==

If the player is a [[Balance]]-specialized [[Druid]], this function returns either "moon" or "sun". If the player is not specialized into the Balance talent tree, or is not a Druid, this function returns "none".

It is unknown at this time whether the return values from this function are localized.

Note that the return value from this function indicates which Eclipse state the player is heading toward, not which Eclipse state the player is currently in, if any.

In the game's default [[User interface|UI]], the value returned by this function corresponds with the direction the pointer on the player's [[Eclipse Bar]] is facing.

==Patch changes==
* {{Patch 7.0.3|note=Removed.}}
```