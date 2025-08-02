# API GetFontStringMetatable

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the metatable used by [[UIOBJECT_FontString|FontString]] objects.
 metatable = GetFontStringMetatable()

==Returns==
:;metatable:{{apitype|table}} - The metatable used by FontString objects.

==Details==
* The metatable returned by this function is shared between all non-forbidden FontString object instances.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}
```