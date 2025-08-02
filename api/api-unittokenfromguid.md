# API UnitTokenFromGUID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Finds a unit token that maps to the supplied unit GUID.
 unitToken = UnitTokenFromGUID(unitGUID)

==Arguments==
:;unitGUID:{{apitype|string}} : [[GUID]] - A unit GUID to query.

==Returns==
:;unitToken:{{apitype|string?}} : [[UnitId]] - A unit token that matches the supplied unit GUID if one can be found, or nil if not.

==Details==
* The return from this function is inherently unstable and may change during processing of UI events or across frames. If storing the result of this function in a table or upvalue, you should confirm before using the stored unit token that it still maps to the unit GUID that was initially requested.
* Internally this function will iterate over a list of unit tokens to find a matching candidate. Unit tokens will be tested in the order given below, returning the first one that matches.
:# player
:# vehicle
:# pet
:# party<font color="#ecbc2a">&lt;x&gt;</font>
:# partypet<font color="#ecbc2a">&lt;x&gt;</font>
:# raid<font color="#ecbc2a">&lt;x&gt;</font>
:# raidpet<font color="#ecbc2a">&lt;x&gt;</font>
:# nameplate<font color="#ecbc2a">&lt;x&gt;</font>
:# arena<font color="#ecbc2a">&lt;x&gt;</font>
:# arenapet<font color="#ecbc2a">&lt;x&gt;</font>
:# boss<font color="#ecbc2a">&lt;x&gt;</font>
:# target
:# focus
:# npc
:# mouseover
:# softenemy
:# softfriend
:# softinteract

==Patch changes==
* {{Patch 10.0.2|note=Added.}}
```