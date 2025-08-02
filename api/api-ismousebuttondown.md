# API IsMouseButtonDown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether a mouse button is being held down.
 isDown = IsMouseButtonDown([button])

==Arguments==
:;button:{{apitype|string?}} - Name of the button. If not passed, then it returns if any mouse button is pressed.
:: {{:Const_MOUSE_BUTTON}}

==Returns==
:;isDown:{{apitype|boolean}} - Returns whether the given mouse button is held down.

==Patch changes==
* {{Patch 2.0.1|note=Added.}}
```