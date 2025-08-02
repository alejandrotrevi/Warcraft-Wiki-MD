# API C KeyBindings.GetCustomBindingType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the type of a custom binding.
 customBindingType = C_KeyBindings.GetCustomBindingType(bindingIndex)

==Arguments==
:;[[API GetNumBindings|bindingIndex]]:{{apitype|number}}

==Returns==
:;customBindingType:Enum.CustomBindingType (nilable)

{| class="sortable darktable zebra"
|-
! Value !! Field !! Description
|-
| <center>0</center> || VoicePushToTalk ||
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```