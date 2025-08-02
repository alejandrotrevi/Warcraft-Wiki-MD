# API C Navigation.GetTargetState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Navigation|system=InGameNavigation}}
Returns state information about the currently tracked location, such as its occlusion status.
 state = C_Navigation.GetTargetState()

==Returns==
:;state:{{apitype|Enum.NavigationState}}
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || Invalid || 
|-
| 1 || Occluded || 
|-
| 2 || InRange || 
|-
| 3 || Disabled || <font color="green">10.0.2</font>
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```