# API FollowUnit

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Follows a friendly player unit.
 FollowUnit(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - The unit to follow.

==Details==
* You can stop follow by following the player itself: <code>FollowUnit("player")</code>. This can have side effects if the character is in a vehicle.
*<s>It is '''not possible''' to ''stop'' following someone from a script. The player needs to take action (move, jump, sit, whatever). See the [[Talk: API FollowUnit|{{discussiontab}} page]].</s>

* For historical reference, see also [[API FollowByName|FollowByName]](), which has been removed from the API.
```