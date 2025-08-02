# API C DeathInfo.GetSelfResurrectOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns self resurrect options for your character, including from soulstones.

 options = C_DeathInfo.GetSelfResurrectOptions()

==Returns==
:;options:structure - SelfResurrectOption[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|-
| name || {{apitype|string}} ||
|-
| optionType || Enum.SelfResurrectOptionType ||
|-
| id || {{apitype|number}} ||
|-
| canUse || {{apitype|boolean}} ||
|-
| isLimited || {{apitype|boolean}} ||
|-
| priority || {{apitype|number}} ||
|}

{{:Enum_DeathInfo.SelfResurrectOptionType}}

==Patch changes==
* {{Patch 7.3.5|note=Added. Replaces {{api|HasSoulstone}} and {{api|CanUseSoulstone}}. [https://www.townlong-yak.com/framexml/7.3.5/Blizzard_Deprecated/Deprecated_7_3_5.lua#11]}}
```