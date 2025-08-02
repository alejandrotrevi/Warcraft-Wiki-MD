# API C PvP.GetScoreInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns PvP score info.
 info = C_PvP.GetScoreInfo(offsetIndex)
      = C_PvP.GetScoreInfoByPlayerGuid(guid)

==Arguments==
===<font color="#4ec9b0">GetScoreInfo</font>===
:;offsetIndex:{{apitype|number}}
===<font color="#4ec9b0">GetScoreInfoByPlayerGuid</font>===
:;guid:{{apitype|string}} : [[GUID#Player|GUID]]

==Returns==
:;info:{{apitype|PVPScoreInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| guid || {{apitype|WOWGUID}} || 
|-
| killingBlows || {{apitype|number}} || 
|-
| honorableKills || {{apitype|number}} || 
|-
| deaths || {{apitype|number}} || 
|-
| honorGained || {{apitype|number}} || 
|-
| faction || {{apitype|number}} || 
|-
| raceName || {{apitype|string}} || 
|-
| className || {{apitype|string}} || 
|-
| classToken || {{apitype|string}} || 
|-
| damageDone || {{apitype|number}} || 
|-
| healingDone || {{apitype|number}} || 
|-
| rating || {{apitype|number}} || 
|-
| ratingChange || {{apitype|number}} || 
|-
| prematchMMR || {{apitype|number}} || 
|-
| mmrChange || {{apitype|number}} || 
|-
| postmatchMMR || {{apitype|number}} || <font color="green">10.1.0</font>
|-
| talentSpec || {{apitype|string}} || 
|-
| honorLevel || {{apitype|number}} || 
|-
| roleAssigned || {{apitype|number}} || 
|-
| stats || {{apitype|PVPStatInfo[]}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ PVPStatInfo
! Field !! Type !! Description
|-
| pvpStatID || {{apitype|number}} || 
|-
| pvpStatValue || {{apitype|number}} || 
|-
| orderIndex || {{apitype|number}} || 
|-
| name || {{apitype|string}} || 
|-
| tooltip || {{apitype|string}} || 
|-
| iconName || {{apitype|string}} || 
|}

==Patch changes==
* {{Patch 9.2.0|note=Added <code>roleAssigned</code> field.}}
* {{Patch 8.2.5|note=Added <code>orderIndex</code> field.}}
* {{Patch 8.2.0|note=Added.}}
```