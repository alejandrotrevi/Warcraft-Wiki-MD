# API GetUnitSpeed

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the movement speed of the unit.
 currentSpeed, runSpeed, flightSpeed, swimSpeed = GetUnitSpeed(unit)

==Arguments==
:;unit:{{apitype|UnitToken}} - The unit to query the speed of.

==Returns==
:;currentSpeed:{{apitype|number}} - current movement speed in yards per second (normal running: 7; an epic ground mount: 14)
:;runSpeed:{{apitype|number}} - the maximum speed on the ground, in yards per second (including talents such as Pursuit of Justice and ground mounts)
:;flightSpeed:{{apitype|number}} - the maximum speed while flying, in yards per second (the unit need to be on a flying mount to get the flying speed)
:;swimSpeed:{{apitype|number}} - the maximum speed while swimming, in yards per second (not tested but it should be as the flying mount)

==Example==
The following snippet prints your current movement speed in percent:
 /script print(string.format("Current speed: %d%%", GetUnitSpeed("player") / 7 * 100))

==Details==
As of 4.2, runSpeed, flightSpeed, swimSpeed returns were added. It seem you can also get target unit speed (not tested on the opposite faction).<br>
A constant exists: "BASE_MOVEMENT_SPEED" which is equal to 7 (4.2).
```