# API GetPrimaryTalentTree

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index of your primary talent tree.
 primaryTabId = GetPrimaryTalentTree([isInspect[, isPet[, talentGroup]]])

==Arguments==
;isInspect : Boolean (Optional) - If true returns the information for the inspected unit instead of the player.
;isPet : Boolean (Optional) - If true returns the information for the inspected pet.
;talentGroup  :  Number (Optional) - The number of the talentgroup you want to look at. i.e. 1 for Primary, 2 for Secondary.

==Returns==
;primaryTabId   : Number - Returns the index of the tab with the most number of talents in it, i.e. the primary talent tree (1, 2, or 3), or nil if no primary tree has been selected.

==Details==
* Talent information is not available until {{api|t=e|PLAYER_ALIVE}} has fired.

==Patch changes==
* {{Patch 5.0.4|note=Replaced by {{api|GetSpecialization}}.}}
* {{Patch 4.0.1|note=Added.}}
```