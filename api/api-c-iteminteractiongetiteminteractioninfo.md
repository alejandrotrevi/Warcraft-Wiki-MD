# API C ItemInteraction.GetItemInteractionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ItemInteraction|system=ItemInteractionUI}}
Needs summary.
 info = C_ItemInteraction.GetItemInteractionInfo()

==Returns==
:;info:{{apitype|ItemInteractionFrameInfo?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| textureKit || {{apitype|string}} || 
|-
| openSoundKitID || {{apitype|number}} || 
|-
| closeSoundKitID || {{apitype|number}} || 
|-
| titleText || {{apitype|string}} || 
|-
| tutorialText || {{apitype|string}} || 
|-
| buttonText || {{apitype|string}} || 
|-
| interactionType || {{apitype|Enum.UIItemInteractionType}} || 
|-
| flags || {{apitype|number}} || 
|-
| description || {{apitype|string?}} || 
|-
| buttonTooltip || {{apitype|string?}} || 
|-
| confirmationDescription || {{apitype|string?}} || 
|-
| slotTooltip || {{apitype|string?}} || <font color="green">10.0.2</font>
|-
| cost || {{apitype|number?}} || 
|-
| currencyTypeId || {{apitype|number?}} || 
|-
| dropInSlotSoundKitId || {{apitype|number?}} || 
|}

{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
|+ Enum.UIItemInteractionType
! Value !! Field !! Description
|-
| 0 || None || 
|-
| 1 || CastSpell || 
|-
| 2 || CleanseCorruption || 
|-
| 3 || RunecarverScrapping || 
|-
| 4 || ItemConversion || <font color="green">9.2.0</font>
|}

==Patch changes==
* {{Patch 9.1.5|note=Added <code>buttonTooltip, confirmationDescription, flags, interactionType</code> fields.}}
* {{Patch 9.0.1|note=Added <code>textureKit</code> field.}}
* {{Patch 8.3.0|note=Added.}}
```