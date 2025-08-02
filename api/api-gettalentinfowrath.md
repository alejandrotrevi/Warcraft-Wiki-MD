# API GetTalentInfo/Wrath

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a talent.
 name, iconTexture, tier, column, rank, maxRank, isExceptional, available, previewRank, previewAvailable 
    = GetTalentInfo(tabIndex, talentIndex [, isInspect[, isPet[, groupIndex]]])

==Arguments==
:;tabIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalentTabs}}()
:;talentIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalents}}(tabIndex).
:;isInspect:{{apitype|boolean?|default=false}} - If true, returns info for the current inspect target (see {{api|NotifyInspect}}).
:;isPet:{{apitype|boolean?|default=false}} - If true, returns info for the player pet.
:;groupIndex:{{apitype|number?|default=1}} - Which dualspec talent group to query (<code>1</code> for primary, <code>2</code> for secondary). If <code>isInspect</code> is <code>false</code> this defaults to the '''currently active''' talent group instead.

==Returns==
:;1. name:{{apitype|string}}
:;2. iconTexture:{{apitype|number}} : [[FileID]]
:;3. tier:{{apitype|number}} - The row/tier that the talent sits on.
:;4. column:{{apitype|number}} - The column that the talent sits on.
:;5. rank:{{apitype|number}} - The current amount of talent points for a talent.
:;6. maxRank:{{apitype|number}} - The maximum amount of talent points for a talent.
:;7. isExceptional:{{apitype|number}} - Returns <code>1</code> if the talent is the ultimate talent, e.g. [[Penance]], otherwise returns <code>nil</code>. Many talents can be tagged as such in a single row.
:;8. available:{{apitype|number}} - Supposed to return whether prerequisites are met. Always returns <code>1</code> for the player. When inspecting it is <code>1</code> if any points have been spent on it, otherwise <code>nil</code>.
:;9. previewRank:{{apitype|number}} - In talent preview mode it returns the previewed points on a talent, otherwise it returns the same as <code>rank</code>.
:;10. previewAvailable:{{apitype|number}} - Supposed to act as <code>available</code> in preview mode. Returns same as <code>available</code> because <code>available</code> doesn't seem to change based on points spent.

==Details==
* The talent index supplied to this function should not be expected to map to the placement of a talent within its tree. Callers must use the <font color="#4ec9b0">tier</font> and <font color="#4ec9b0">column</font> return values to determine where a queried talent is located.

==Example==
Prints all existing talents of your class.
<syntaxhighlight lang="lua">
for i = 1, GetNumTalentTabs() do
	for j = 1, GetNumTalents(i) do
		print(i, j, GetTalentInfo(i, j))
	end
end
</syntaxhighlight>

==Patch changes==
* {{Patch 1.13.2|note=Added.}}
```