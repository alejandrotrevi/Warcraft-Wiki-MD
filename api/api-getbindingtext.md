# API GetBindingText

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the string for the given key and prefix. Essentially a specialized getglobal() for bindings.
 text = GetBindingText([key, prefix, abbreviate])

==Arguments==
:;key:{{apitype|string?}} - The name of the key (e.g. "UP", "SHIFT-PAGEDOWN")
:;prefix:{{apitype|string?}} - The prefix of the variable name you're looking for.  Usually "KEY_" or "BINDING_NAME_".
:;abbreviate:{{apitype|boolean?}} - Whether to return an abbreviated version of the modifier keys

==Returns==
:;text:{{apitype|string}} - The value of the global variable derived from the prefix and key name you specified. For example, "UP" and "KEY_" would return the value of the global variable KEY_UP which is "Up Arrow" in the english locale.  If the global variable doesn't exist for the combination specified, it appears to just return the key name you specified. Modifier key prefixes are stripped from the input and added back in to the output. <br>The third parameter, if true, causes the function to simply substitute the abbreviations 'c', 'a', 's', and 'st' for the strings CTRL, ALT, SHIFT, and STRG (German client only) in the result.

==Example==
 /dump GetBindingText("UP", "KEY_")

 > "Up Arrow"

==Patch changes==
* {{Patch 6.0.2|note=Added. Replaces the FrameXML version of the same name<sup>[https://github.com/Gethe/wow-ui-source/blob/5.2.0/FrameXML/UIParent.lua#L3225]</sup>}}
```