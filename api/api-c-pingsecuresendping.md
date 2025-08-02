# API C PingSecure.SendPing

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PingSecure|system=PingManager}} {{restrictedapi|protected}}
Sends a ping to all members of your current group.
 result = C_PingSecure.SendPing(type [, target])

==Arguments==
:;type:{{apitype|Enum.PingSubjectType}}
{{:Enum.PingSubjectType|nocaption=1}}
:;target:{{apitype|WOWGUID?}}

==Returns==
:;result:{{apitype|Enum.PingResult}}
{{:Enum.PingResult|nocaption=1}}

==Details==
* To submit a ping to an in-world location, first call {{api|C_PingSecure.GetTargetWorldPing}} with the screen position to place the ping at. If it returns true, call this function with the target parameter omitted or set to nil.
* To submit a ping that will display over a unit, the target parameter must be a valid unit [[GUID]].
* Pings for units only support a limited subset of unit types. Creatures, Pets, Players, and Vehicles can all be pinged, but GameObjects such as gathering nodes and treasure chests cannot.

==Patch changes==
* {{Patch 10.1.7|note=Added.}}
```