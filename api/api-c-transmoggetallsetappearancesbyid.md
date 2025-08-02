# API C Transmog.GetAllSetAppearancesByID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Needs summary.
 setItems = C_Transmog.GetAllSetAppearancesByID(setID)

==Arguments==
:;setID:{{apitype|number}}

==Returns==
:;setItems:{{apitype|TransmogSetItemInfo[]?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| <code>itemID</code> || {{apitype|number}} || 
|-
| <code>itemModifiedAppearanceID</code> || {{apitype|number}} || 
|-
| <code>invSlot</code> || {{apitype|number}} || 
|-
| <code>invType</code> || {{apitype|string}} || 
|}
```