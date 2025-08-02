# API GetTalentInfo/Classic

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a talent.
 name, iconTexture, tier, column, rank, maxRank, isExceptional, available = GetTalentInfo(tabIndex, talentIndex [, isInspect])

==Arguments==
:;tabIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalentTabs}}()
:;talentIndex:{{apitype|number}} - Ranging from 1 to {{api|GetNumTalents}}(tabIndex).
:;isInspect:{{apitype|boolean?}} - If true, returns info for the current inspect target (see {{api|NotifyInspect}}).

==Returns==
:;name:{{apitype|string}}
:;iconTexture:{{apitype|number}} : [[FileID]]
:;tier:{{apitype|number}} - The row/tier that the talent sits on.
:;column:{{apitype|number}} - The column that the talent sits on.
:;rank:{{apitype|number}} - The current amount of talent points for a talent.
:;maxRank:{{apitype|number}} - The maximum amount of talent points for a talent.
:;isExceptional:{{apitype|number}} - Returns <code>1</code> if the talent is the ultimate talent, e.g. [[Lightwell]], otherwise returns <code>nil</code>.
:;available:{{apitype|number}}

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