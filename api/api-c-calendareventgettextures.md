# API C Calendar.EventGetTextures

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 textures = C_Calendar.EventGetTextures(eventType)

==Arguments==
:;eventType:enum - CalendarEventType
{{:Enum_Calendar.CalendarEventType}}

==Returns==
:;textures:structure - CalendarEventTextureInfo[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| title || {{apitype|string}} ||
|-
| iconTexture || {{apitype|number}} ||
|-
| expansionLevel || {{apitype|number}} ||
|-
| difficultyId || {{apitype|number?}} ||
|-
| mapId || {{apitype|number?}} ||
|-
| isLfr || {{apitype|number?}} ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```