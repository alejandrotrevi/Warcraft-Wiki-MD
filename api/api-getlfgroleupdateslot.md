# API GetLFGRoleUpdateSlot

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the objectives you are currently flagged to as LFG.
 dungeonID, dungeonType, dungeonSubType = GetLFGRoleUpdateSlot(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;dungeonID:{{apitype|number}} : [[LfgDungeonID]]
:;dungeonType:{{apitype|number}}
:;dungeonSubType:{{apitype|number}}

==Details==
Known dungeon types are defined in [https://github.com/Gethe/wow-ui-source/blob/9.2.0/Interface/FrameXML/Constants.lua#L777 Constants.lua]
<syntaxhighlight lang="lua">
TYPEID_DUNGEON = 1;
TYPEID_RANDOM_DUNGEON = 6;

LFG_SUBTYPEID_DUNGEON = 1;
LFG_SUBTYPEID_HEROIC = 2;
LFG_SUBTYPEID_RAID = 3;
LFG_SUBTYPEID_SCENARIO = 4;
LFG_SUBTYPEID_FLEXRAID = 5;
LFG_SUBTYPEID_WORLDPVP = 6;
</syntaxhighlight>
```