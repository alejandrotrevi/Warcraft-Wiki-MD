# API C TransmogCollection.GetIllusions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns transmoggable enchants for the appearances tab.
 visualsList = C_TransmogCollection.GetIllusions()

==Returns==
:;visualsList:structure[]

{| class="sortable darktable zebra"
|-
! Field !! Type !! Description
|- 
| isCollected || {{apitype|boolean}} ||
|-
| isUsable || {{apitype|boolean}} ||
|-
| sourceID || {{apitype|number}} ||
|-
| sourceText || {{apitype|string}} ||
|-
| [[WeaponEnchantID|visualID]] || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}

==See also==
* {{api|C_TransmogCollection.GetIllusionSourceInfo}}
```