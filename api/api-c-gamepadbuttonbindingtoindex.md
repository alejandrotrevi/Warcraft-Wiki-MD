# API C GamePad.ButtonBindingToIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GamePad|system=GamePad}}
Converts the name of a keybinding to its assigned gamepad button index. Returns nil if no gamepad button is assigned to the requested keybinding.
 buttonIndex = C_GamePad.ButtonBindingToIndex(bindingName)

==Arguments==
:;bindingName:{{apitype|string}}

==Returns==
:;buttonIndex:{{apitype|number?}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}

{{apinavbox|C_GamePad}}
```