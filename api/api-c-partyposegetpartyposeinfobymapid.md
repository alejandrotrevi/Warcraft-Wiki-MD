# API C PartyPose.GetPartyPoseInfoByMapID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns party pose info for an [[Island Expedition]] or [[Warfront]].
 info = C_PartyPose.GetPartyPoseInfoByMapID(mapID)

==Arguments==
:;mapID:{{apitype|number}}

==Returns==
:;info:{{apitype|PartyPoseInfo}}
{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| partyPoseID || {{apitype|number}} || {{dbc|uipartypose|UIPartyPose.db2}}
|-
| mapID || {{apitype|number}} || May return 0
|-
| widgetSetID || {{apitype|number?}} ||
|-
| victoryModelSceneID || {{apitype|number}} ||
|-
| defeatModelSceneID || {{apitype|number}} ||
|-
| victorySoundKitID || {{apitype|number}} || See {{api|PlaySound(soundKitID)}}
|-
| defeatSoundKitID || {{apitype|number}} ||
|}

==Gallery==
<gallery>
Island Expedition UI Horde victory.jpg|Horde party pose
Island Expedition UI Alliance victory.jpg|Alliance party pose
</gallery>

==Patch changes==
* {{Patch 8.0.1|note=Added.<ref>{{ref FrameXML|Blizzard_PartyPoseUI/Blizzard_PartyPoseUI.lua|8.0.1|27101||20180716}}</ref>}}

==References==
{{Reflist}}
```