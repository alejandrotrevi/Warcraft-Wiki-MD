# API C IncomingSummon.IncomingSummonStatus

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the status of an group member's incoming summon.
 status = C_IncomingSummon.IncomingSummonStatus(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;status:Enum.SummonStatus

{| class="sortable darktable zebra"
|-
! Value !! Field !! Description
|-
| <center>0</center> || None ||
|-
| <center>1</center> || Pending ||
|-
| <center>2</center> || Accepted ||
|-
| <center>3</center> || Declined ||
|}

==Patch changes==
* {{Patch 8.1.0|note=Added.}}
```