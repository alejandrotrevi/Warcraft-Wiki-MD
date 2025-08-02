# API C PvP.GetActiveMatchState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 state = C_PvP.GetActiveMatchState()

==Returns==
:;state:{{apitype|Enum.PvPMatchState}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Inactive || 
|-
| 1 || Waiting || <font color="green">10.1.5</font>
|-
| 2 || StartUp || <font color="green">10.1.5</font>
|-
| 3 || Engaged || <font color="green">10.1.5</font>
|-
| 4 || PostRound || <font color="green">10.1.5</font>
|-
| 5 || Complete || 
|}

==Patch changes==
* {{Patch 10.1.5|note=Removed <code>Active</code> enum.}}
* {{Patch 8.2.0|note=Added.}}
```