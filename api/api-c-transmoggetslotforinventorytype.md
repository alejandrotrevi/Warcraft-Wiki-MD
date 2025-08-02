# API C Transmog.GetSlotForInventoryType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Transmog|system=Transmogrify}}
Returns the equipment slot for an inventory type.
 slot = C_Transmog.GetSlotForInventoryType(inventoryType)

==Arguments==
:;inventoryType:{{apitype|number}} : [[Enum.InventoryType]]

==Returns==
:;slot:{{apitype|number}} - The [[inventorySlotId|equipmentSlot]] for an inventory type.

==Values==
{{i-note|This function uses Enum.InventoryType off-by-one; 1-29 instead of 0-28}}
{| class="sortable darktable zebra"
|-
! InvType !! InvTypeName !! InvSlotId !! InvSlotName
|-
| align="center" | 2 || IndexHeadType || align="center" | 1 || HEADSLOT
|-
| align="center" | 4 || IndexShoulderType || align="center" | 3 || SHOULDERSLOT
|-
| align="center" | 5 || IndexBodyType || align="center" | 4 || SHIRTSLOT
|-
| align="center" | 6 || IndexChestType || align="center" | 5 || CHESTSLOT
|-
| align="center" | 7 || IndexWaistType || align="center" | 6 || WAISTSLOT
|-
| align="center" | 8 || IndexLegsType || align="center" | 7 || LEGSSLOT
|-
| align="center" | 9 || IndexFeetType || align="center" | 8 || FEETSLOT
|-
| align="center" | 10 || IndexWristType || align="center" | 9 || WRISTSLOT
|-
| align="center" | 11 || IndexHandType || align="center" | 10 || HANDSSLOT
|-
| align="center" | 14 || IndexWeaponType || align="center" | 16 || MAINHANDSLOT
|-
| align="center" | 15 || IndexShieldType || align="center" | 17 || SECONDARYHANDSLOT
|-
| align="center" | 16 || IndexRangedType || align="center" | 16 || MAINHANDSLOT
|-
| align="center" | 17 || IndexCloakType || align="center" | 15 || BACKSLOT
|-
| align="center" | 18 || Index2HweaponType || align="center" | 16 || MAINHANDSLOT
|-
| align="center" | 20 || IndexTabardType || align="center" | 19 || TABARDSLOT
|-
| align="center" | 21 || IndexRobeType || align="center" | 5 || CHESTSLOT
|-
| align="center" | 22 || IndexWeaponmainhandType || align="center" | 16 || MAINHANDSLOT
|-
| align="center" | 23 || IndexWeaponoffhandType || align="center" | 16 || MAINHANDSLOT
|-
| align="center" | 24 || IndexHoldableType || align="center" | 17 || SECONDARYHANDSLOT
|-
| align="center" | 27 || IndexRangedrightType || align="center" | 16 || MAINHANDSLOT
|}

==Patch changes==
* {{Patch 7.2.0|note=Added.}}
```