# API C GamePad.ButtonIndexToBinding

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GamePad|system=GamePad}}
Returns the name of the keybinding assigned to a specified gamepad button index. Returns nil if no keybinding is assigned to the requested button.
 bindingName = C_GamePad.ButtonIndexToBinding(buttonIndex)

==Arguments==
:;buttonIndex:{{apitype|number}}

==Returns==
:;bindingName:{{apitype|string?}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}

{{apinavbox|C_GamePad}}
```