# API C LFGList.GetActivityInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about an activity for [[Premade_Groups|premade groups]].
 fullName, shortName, categoryID, groupID, itemLevel, filters, minLevel, maxPlayers, displayType, orderIndex, useHonorLevel, showQuickJoinToast, isMythicPlusActivity, isRatedPvpActivity, isCurrentRaidActivity = C_LFGList.GetActivityInfo(activityID)

==Arguments==
;activityID : <span class="apitype">number</span> : {{dbc|groupfinderactivity|GroupFinderActivity.ID}} - The activityID for which information are requested, as returned by [[API_C_LFGList.GetAvailableActivities|C_LFGList.GetAvailableActivities]]().

==Returns==
;fullName : <span class="apitype">string</span> - Full name of the activity.
;shortName : <span class="apitype">string</span> - Short name of the activity, for example just "World Bosses" instead of the fullName "World Bosses (Pandaria)".
;categoryID : <span class="apitype">number</span> - The categoryID of this activity, as returned by [[API_C_LFGList.GetAvailableCategories|C_LFGList.GetAvailableCategories]]().
;groupID : <span class="apitype">number</span> - The groupID of this activity, as returned by [[API_C_LFGList.GetAvailableActivityGroups|C_LFGList.GetAvailableActivityGroups]]().
;itemLevel : <span class="apitype">number</span> - Minimum [[item_level]] required for this activity. Return 0 if no requirement.
;filters : <span class="apitype">number</span> - Bit mask of filters for this activity. See details.
;minLevel : <span class="apitype">number</span> - Minimum [[level]] required for this activity.
;maxPlayers : <span class="apitype">number</span> - Maximum number of players allowed for this activity.
;displayType : <span class="apitype">number</span> - The display type ID for this activity. See details.
;orderIndex : <span class="apitype">number</span> - How the activity is ordered. See details.
;useHonorLevel : <span class="apitype">boolean</span>
;showQuickJoinToast : <span class="apitype">boolean</span>
;isMythicPlusActivity : <span class="apitype">boolean</span>
;isRatedPvpActivity : <span class="apitype">boolean</span>
;isCurrentRaidActivity : <span class="apitype">boolean</span>

==Details==
===Filters===
{{Stub-section}}
{| class="darktable zebra"
! Name !! Value !! Info
|-
| LE_LFG_LIST_FILTER_RECOMMENDED || 1 || ?
|-
| LE_LFG_LIST_FILTER_NOT_RECOMMENDED || 2 || ?
|-
| LE_LFG_LIST_FILTER_PVE || 4 || ?
|-
| LE_LFG_LIST_FILTER_PVE || 8 || ?
|}

===DisplayType===
The display type determines how the current size of a group is displayed in the list. This number is going from 1 to NUM_LE_LFG_LIST_DISPLAY_TYPES:
{| class="darktable zebra"
! Name !! Value !! Info
|-
| LE_LFG_LIST_DISPLAY_TYPE_ROLE_COUNT || 1 || Display how many of each [[class role]] are present in the group. This is used for custom groups for example.
|-
| LE_LFG_LIST_DISPLAY_TYPE_ROLE_ENUMERATE || 2 || Each present and each missing player in the group is depicted with a role icon. This is used for 5man dungeons for exmample.
|-
| LE_LFG_LIST_DISPLAY_TYPE_CLASS_ENUMERATE || 3 || ?
|-
| LE_LFG_LIST_DISPLAY_TYPE_HIDE_ALL || 4 || Hide all group size indicators.
|-
| LE_LFG_LIST_DISPLAY_TYPE_PLAYER_COUNT || 5 || Only display the total number of players in group. This is used for questing groups for example.
|}

===ActivityOrder===
{{Stub-section}}

==Patch changes==
* {{Patch 9.1.5|note=Deprecated, replaced by {{api|C_LFGList.GetActivityInfoTable}}().}}
```