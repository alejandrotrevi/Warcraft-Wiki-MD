# API IsInInstance

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns true if the player is in an instance, and the type of instance.
 inInstance, instanceType = IsInInstance()

==Returns==
:;inInstance:{{apitype|boolean}} - Whether the player is in an instance; nil otherwise.
:;instanceType:{{apitype|string}} - The instance type:
::* "none" when outside an instance
::* "pvp" when in a battleground
::* "arena" when in an arena
::* "party" when in a 5-man instance
::* "raid" when in a raid instance
::* "scenario" when in a scenario

==Details==
This functon returns correct results immediately upon PLAYER_ENTERING_WORLD.
```