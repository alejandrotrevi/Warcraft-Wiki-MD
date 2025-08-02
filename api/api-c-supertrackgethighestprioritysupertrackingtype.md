# API C SuperTrack.GetHighestPrioritySuperTrackingType

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SuperTrack|system=SuperTrackManager}}
Returns the type of the location currently being tracked as the highest priority, if one exists.
 type = C_SuperTrack.GetHighestPrioritySuperTrackingType()

==Returns==
:;type:{{apitype|Enum.SuperTrackingType?}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|Quest}} || 
|-
| 1 || {{apiname|UserWaypoint}} || 
|-
| 2 || {{apiname|Corpse}} || 
|-
| 3 || {{apiname|Scenario}} || 
|-
| 4 || {{apiname|Content}} || <font color="green">10.1.5</font>
|-
| 5 || {{apiname|PartyMember}} || <font color="green">10.2.6</font>
|-
| 6 || {{apiname|MapPin}} || <font color="green">11.0.0</font>
|-
| 7 || {{apiname|Vignette}} || <font color="green">11.0.0</font>
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```