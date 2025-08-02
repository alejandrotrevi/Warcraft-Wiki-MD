# API EJ SetSlotFilter

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the Encounter Journal's equipment slot filter.
 EJ_SetSlotFilter(slotFilterID)

== Arguments ==
;slotFilterID : Number - One of the following filter IDs indicating which items should be returned by {{api|EJ_GetLootInfoByIndex}}.

{| class="wikitable" style="margin-left: 2em"
|-
! Global Constant !! Value !! Description
|-
| n/a || 0|| All Slots
|-
| LE_ITEM_FILTER_TYPE_HEAD || 1|| Head
|-
| LE_ITEM_FILTER_TYPE_NECK || 2|| Neck
|-
| LE_ITEM_FILTER_TYPE_SHOULDER || 3|| Shoulder
|-
| LE_ITEM_FILTER_TYPE_CHEST || 5|| Chest
|-
| LE_ITEM_FILTER_TYPE_WAIST || 6|| Waist
|-
| LE_ITEM_FILTER_TYPE_LEGS || 7|| Legs
|-
| LE_ITEM_FILTER_TYPE_FEET || 8|| Feet
|-
| LE_ITEM_FILTER_TYPE_WRIST || 9|| Wrist
|-
| LE_ITEM_FILTER_TYPE_HAND || 10|| Hands
|-
| LE_ITEM_FILTER_TYPE_FINGER || 11|| Finger
|-
| LE_ITEM_FILTER_TYPE_TRINKET || 12|| Trinket
|-
| LE_ITEM_FILTER_TYPE_CLOAK || 16|| Back
|-
| LE_ITEM_FILTER_TYPE_MAIN_HAND || 21|| Main Hand
|-
| LE_ITEM_FILTER_TYPE_OFF_HAND || 22|| Off Hand
|-
| LE_ITEM_FILTER_TYPE_ARTIFACT_RELIC || 30|| Artifact Relic
|}

== See also ==
* {{api|EJ_GetSlotFilter}}
* {{api|EJ_GetNumLoot}}

==Patch changes==
* {{Patch 7.1.0|note=Added.}}
```