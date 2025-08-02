# API UnitIsVisible

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns true if the unit is visible to the game client.
 visible = UnitIsVisible(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;visible:{{apitype|boolean}}

==Details==
* A unit is considered visible if the client has received information from the server on the existence of a unit, typically by being within the local area of the unit or it being a member of your party or raid. The API will continue to return true until the unit is unloaded.
* Visibility does not imply that the player has line-of-sight of the unit.
* Unlike {{api|t=a|UnitExists}}, this API will return true for units that exist but cannot be targeted.
```