# API GetButtonMetatable

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the metatable used by [[UIOBJECT_Button|Button]] objects.
 metatable = GetButtonMetatable()

==Returns==
:;metatable:{{apitype|table}} - The metatable used by Button objects.

==Details==
* The metatable returned by this function is shared between all non-forbidden Button object instances.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}
```