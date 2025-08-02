# API GetPlayerFacing

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}} {{restrictedapi|noinstance}}
Returns the direction the character is facing in radians.
 facing = GetPlayerFacing()

==Returns==
:;facing:{{apitype|number}} - Direction the player is facing in radians, in the [0, 2π] range, where 0 is North and values increase counterclockwise.

==Details==
* Indicates the direction the player model is (normally) facing and in which the player will move if he begins walking forward; ''not'' the camera orientation.

==Patch changes==
* {{Patch 7.1.0|note=Returns nil while in a restricted area (instance/battleground/arena).}}
* {{Patch 3.1.0|note=Added.}}
```