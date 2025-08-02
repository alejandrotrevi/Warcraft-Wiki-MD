# API GetEditBoxMetatable

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the metatable used by [[UIOBJECT_EditBox|EditBox]] objects.
 metatable = GetEditBoxMetatable()

==Returns==
:;metatable:{{apitype|table}} - The metatable used by EditBox objects.

==Details==
* The metatable returned by this function is shared between all non-forbidden EditBox object instances.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}
```