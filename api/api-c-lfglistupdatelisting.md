# API C LFGList.UpdateListing

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{ood|Needs to be updated for 11.0.7}}
Updates information for the players' currently listed group.
 -- Retail
 C_LFGList.UpdateListing(activityID, itemLevel, honorLevel, autoAccept, privateGroup [, questID, mythicPlusRating, pvpRating, selectedPlaystyle, isCrossFaction]) 
 
 -- Classic
 C_LFGList.UpdateListing(activityIDs)

==Arguments==
===<font color="#4ec9b0">Retail</font>===
:;activityID:{{apitype|number}} - Activity ID to register the group for.
:;itemLevel:{{apitype|number}} - Minimum required item level for group applicants.
:;honorLevel:{{apitype|number}} - Minimum required honor level for group applicants.
:;autoAccept:{{apitype|boolean}} - If true, new applicants will be automatically invited to join the group.
:;privateGroup:{{apitype|boolean}} - If true, the listing will only be visible to friends and guild members of players inside the group.
:;questID:{{apitype|number?}}  - Optional quest ID to associate with the group listing.
:;mythicPlusRating:{{apitype|number?}}  - Optional mythic plus rating needed to signup to the group listing.
:;pvpRating:{{apitype|number?}}  - Optional pvp rating needed to signup to the group listing.
:;selectedPlaystyle:{{apitype|number?}}  - Refers to [[Enum.LFGEntryPlaystyle]] values.
:;isCrossFaction:{{apitype|boolean?|default=true}}  - Optional. If false, the group listing will not be visible to players of the opposite faction. If nil, true will be assumed.

===<font color="#4ec9b0">Classic</font>===
:;activityIDs:{{apitype|number[]}} - Table of up to three activity IDs to register the group listing for.

==Details==
* {{bc-inline}} For Classic, a player can register interest in a maximum of three activities at once. Other options for listings such as preferred item level, auto-accept, and private groups do not exist.

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 6.0.2|note=Added.}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 2.5.2|note=Added.}}
<!-- luals
---@param activityID number
---@param itemLevel number
---@param honorLevel number
---@param autoAccept boolean
---@param privateGroup boolean
---@param questID? number
---@param mythicPlusRating? number
---@param pvpRating? number
---@param selectedPlaystyle? number
---@param isCrossFaction boolean?
function C_LFGList.UpdateListing(activityID, itemLevel, honorLevel, autoAccept, privateGroup, questID, mythicPlusRating, pvpRating, selectedPlaystyle, isCrossFaction) end
-->
```