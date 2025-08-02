# API TurnOrActionStart

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Starts a "right click" in the 3D game world.
 TurnOrActionStart()

==Details==
* This function is called when right clicking in the 3D world.
* Calling this function clears the "mouseover" unit.
* When used alone, puts you into a "mouseturn" mode until [[API TurnOrActionStop|TurnOrActionStop]] is called.
* IMPORTANT: The normal restrictions regarding hardware event initiations still apply to anything this function might do.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```