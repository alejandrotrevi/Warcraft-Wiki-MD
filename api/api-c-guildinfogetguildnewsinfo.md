# API C GuildInfo.GetGuildNewsInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 newsInfo = C_GuildInfo.GetGuildNewsInfo(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;newsInfo:structure - GuildNewsInfo
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| isSticky || {{apitype|boolean}} || 
|-
| isHeader || {{apitype|boolean}} || 
|-
| newsType || {{apitype|number}} || 
|-
| whoText || {{apitype|string?}} || 
|-
| whatText || {{apitype|string?}} || 
|-
| newsDataID || {{apitype|number}} || 
|-
| data || {{apitype|number[]}} || 
|-
| weekday || {{apitype|number}} || 
|-
| day || {{apitype|number}} || 
|-
| month || {{apitype|number}} || 
|-
| year || {{apitype|number}} || 
|-
| guildMembersPresent || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 8.2.0|note=Moved to {{api|C_GuildInfo.GetGuildNewsInfo}}. The previous alias is deprecated. [https://www.townlong-yak.com/framexml/8.2.0/Blizzard_Deprecated/Deprecated_8_2_0.lua#45]}}
* {{Patch 4.0.1|note=Added as {{api|GetGuildNewsInfo}}.}}
```