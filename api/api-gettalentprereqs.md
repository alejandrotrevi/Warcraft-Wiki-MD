# API GetTalentPrereqs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the tier and column of a talent's prerequisite, and if the talent is learnable.
 tier, column, isLearnable = GetTalentPrereqs(tabIndex, talentIndex [, isInspect, isPet, talentGroup)

==Arguments==
:;tabIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalentTabs}}()
:;talentIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalents}}(tabIndex)
:;isInspect:{{apitype|boolean?}} - Whether the talent is for the currently inspected player.
:;isPet:{{apitype|boolean?}}
:;talentGroup:{{apitype|number?}} - Probably the dual spec group index.

==Returns==
:;tier:{{apitype|number}} - The row/tier that the prerequisite talent sits on.
:;column:{{apitype|number}} - The column that the prerequisite talent sits on.
:;isLearnable:{{apitype|number}} - Returns 1 if you have learned the prerequisite talents, nil otherwise.

==Details==
* The <code>talentIndex</code> is counted as if it where a tree, meaning that the left most talent in the top most row is number 1 followed by the one immediate to the right is number 2, if there are no more talents to the right then it continues from the left most talent on the next row.
* If you check a talent with no prerequisites, the function returns nil.

==Patch changes==
* {{Patch 5.0.4|note=Removed.}}
```