# API GetFrameMetatable

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the metatable used by [[UIOBJECT_Frame|Frame]] objects.
 metatable = GetFrameMetatable()

==Returns==
:;metatable:{{apitype|table}} - The metatable used by Frame objects.

==Details==
* The metatable returned by this function is shared between all non-forbidden Frame object instances.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}
```