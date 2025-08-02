# API C PingSecure.GetTargetWorldPing

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PingSecure|system=PingManager}} {{restrictedapi|protected}}
Prepares the ping system for a ping in the game world.
 foundTarget = C_PingSecure.GetTargetWorldPing(mousePosX, mousePosY)

==Arguments==
:;mousePosX:{{apitype|number}}
:;mousePosY:{{apitype|number}}

==Returns==
:;foundTarget:{{apitype|boolean}} - True if the supplied position can be pinged.

==Details==
* The coordinates supplied to this function should typically be the return values of {{api|GetCursorPosition}}.
* This function should be followed up by a call to {{api|C_PingSecure.SendPing}} with the target parameter omitted to submit the ping at the requested position.

==Patch changes==
* {{Patch 10.1.7|note=Added.}}
```