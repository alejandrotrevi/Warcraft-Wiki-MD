# API C Garrison.GetFollowerAbilities

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the abilities of a garrison follower.
 abilities, extraAbilities = C_Garrison.GetFollowerAbilities(followerID)

==Arguments==
:;followerID:{{apitype|number,string}} : [[GarrFollowerID|FollowerID]] or [[GUID#Follower|FollowerGUID]]

==Returns==
:;abilities:{{apitype|AbilityInfo[]}} - A table containing information about abilities of a single follower.
:;extraAbilities:{{apitype|AbilityInfo[]?}} - If a FollowerGUID is used, another table of abilities. This seems to be only relevant for BFA followers.

{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| colspan=3 | <center><font color="#FFCCCB">''This structure is manually documented''</font></center>
|-
| category || {{apitype|string?}} || 
|-
| counters || {{apitype|table<number:counterID, AbilityCounter>}} || 
|-
| description || {{apitype|string}} || 
|-
| icon || {{apitype|fileID?}} || 
|-
| id || {{apitype|number}} || 
|-
| isEmptySlot || {{apitype|boolean}} || 
|-
| isSpecialization || {{apitype|boolean}} || 
|-
| isTrait || {{apitype|boolean}} || 
|-
| name || {{apitype|string}} || 
|-
| requiredQualityLevel || {{apitype|number?}} || 
|-
| temporary || {{apitype|boolean}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ AbilityCounter
! Field !! Type !! Description
|-
| description || {{apitype|string}} || 
|-
| factor || {{apitype|number}} || 
|-
| icon || {{apitype|fileID}} || 
|-
| name || {{apitype|string}} || 
|}

==Example==
<syntaxhighlight lang="lua">
-- /dump C_Garrison.GetFollowerAbilities(32) -- Dagg
{
  {
    description = "Used by a rogue to neutralize a dangerous enemy (or just to annoy you).",
    counters = {
      [9] = {
        description = "An enemy with powerful allies that should be neutralized.",
        factor = 300,
        icon = 1035504,
        name = "Deadly Minions"
      }
    },
    icon = 132310,
    id = 104,
    isEmptySlot = false,
    isSpecialization = false,
    isTrait = false
    name = "Sap",
    temporary = false,
  }
}
</syntaxhighlight>

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

<!-- luals
---@param followerID number|string
---@return AbilityInfo[] abilities
---@return AbilityInfo[]? extraAbilities
function C_Garrison.GetFollowerAbilities(followerID) end

---@class AbilityInfo
---@field category? string
---@field counters table<number, AbilityCounter>
---@field description string
---@field icon? fileID
---@field id number
---@field isEmptySlot boolean
---@field isSpecialization boolean
---@field isTrait boolean
---@field name string
---@field requiredQualityLevel? number
---@field temporary boolean

---@class AbilityCounter
---@field description string
---@field factor number
---@field icon fileID
---@field name string
-->
```