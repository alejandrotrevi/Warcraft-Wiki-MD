# API C Container.GetContainerItemInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Container|system=Container}}
Needs summary.
 containerInfo = C_Container.GetContainerItemInfo(containerIndex, slotIndex)

==Arguments==
:;containerIndex:{{apitype|number}}
:;slotIndex:{{apitype|number}}

==Returns==
:;containerInfo:{{apitype|ContainerItemInfo?}} - Returns <code>nil</code> if the container slot is empty.
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| iconFileID || {{apitype|number}} || 
|-
| stackCount || {{apitype|number}} || 
|-
| isLocked || {{apitype|boolean}} || 
|-
| quality || {{apitype|Enum.ItemQuality?}} || 
|-
| isReadable || {{apitype|boolean}} || 
|-
| hasLoot || {{apitype|boolean}} || 
|-
| hyperlink || {{apitype|string}} || 
|-
| isFiltered || {{apitype|boolean}} || 
|-
| hasNoValue || {{apitype|boolean}} || 
|-
| itemID || {{apitype|number}} || 
|-
| isBound || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 10.0.2|note=Namespaced to <code>C_Container</code> and returns a structured table.}}
```