# API C ChatInfo.GetChannelInfoFromIdentifier

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChatInfo|system=ChatInfo}}
Needs summary.
 info = C_ChatInfo.GetChannelInfoFromIdentifier(channelIdentifier)

==Arguments==
:;channelIdentifier:{{apitype|string}}

==Returns==
:;info:{{apitype|ChatChannelInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| shortcut || {{apitype|string}} || 
|-
| localID || {{apitype|number}} || 
|-
| instanceID || {{apitype|number}} || 
|-
| zoneChannelID || {{apitype|number}} || 
|-
| channelType || {{apitype|Enum.PermanentChatChannelType}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.PermanentChatChannelType
! Value !! Field !! Description
|-
| 0 || None || 
|-
| 1 || Zone || 
|-
| 2 || Communities || 
|-
| 3 || Custom || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Added.}}
```