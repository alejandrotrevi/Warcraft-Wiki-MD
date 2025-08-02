# API C PvP.GetMatchPVPStatColumn

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 info = C_PvP.GetMatchPVPStatColumn(pvpStatID)

==Arguments==
:;pvpStatID:{{apitype|number}}

==Returns==
:;info:structure - MatchPVPStatColumn (nilable)
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| pvpStatID || {{apitype|number}} || 
|-
| columnHeaderID || {{apitype|number}} || 
|-
| orderIndex || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| tooltip || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 8.2.0|note=Added.}}
```