# API EJ GetInvTypeSortOrder

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the sort order for an inventory type.
 sortOrder = EJ_GetInvTypeSortOrder(invType)

==Arguments==
:;invType:{{apitype|number}} : [[Enum.InventoryType]]

==Returns==
:;sortOrder:{{apitype|number}}

==Values==
{{i-note|This function uses Enum.InventoryType off-by-one; 1-29 instead of 0-28}}
{| class="sortable darktable zebra"
|-
! InvType !! InvTypeName !! SortOrder
|-
| <center>18</center> || Index2HweaponType || 1
|-
| <center>22</center> || IndexWeaponmainhandType || 2
|-
| <center>23</center> || IndexWeaponoffhandType || 3
|-
| <center>14</center> || IndexWeaponType || 4
|-
| <center>16</center> || IndexRangedType || 5
|-
| <center>27</center> || IndexRangedrightType || 5
|-
| <center>15</center> || IndexShieldType || 6
|-
| <center>24</center> || IndexHoldableType || 7
|-
| <center>26</center> || IndexThrownType || 8
|-
| <center>29</center> || IndexRelicType || 9
|-
| <center>2</center> || IndexHeadType || 10
|-
| <center>3</center> || IndexNeckType || 11
|-
| <center>4</center> || IndexShoulderType || 12
|-
| <center>17</center> || IndexCloakType || 13
|-
| <center>6</center> || IndexChestType || 14
|-
| <center>21</center> || IndexRobeType || 14
|-
| <center>10</center> || IndexWristType || 15
|-
| <center>11</center> || IndexHandType || 16
|-
| <center>7</center> || IndexWaistType || 17
|-
| <center>8</center> || IndexLegsType || 18
|-
| <center>9</center> || IndexFeetType || 19
|-
| <center>12</center> || IndexFingerType || 20
|-
| <center>13</center> || IndexTrinketType || 21
|}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```