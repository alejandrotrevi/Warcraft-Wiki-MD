# API TurnOrActionStop

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Stops a "right click" in the 3D game world.
 TurnOrActionStop()

==Details==
* This function is called when right clicking in the 3D world. Most usefull it can initiate attack on the selected unit if no move occurs.
* When used alone, can cancel a "mouseturn" started by a call to [[API TurnOrActionStart|TurnOrActionStart]].
* IMPORTANT: The normal restrictions regarding hardware event initiations still apply to anything this function might do.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```