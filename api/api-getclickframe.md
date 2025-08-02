# API GetClickFrame

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the frame registered with the given object name.
 frame = GetClickFrame(name)

==Arguments==
:;name:{{apitype|string}} - The name of the frame to obtain.

==Returns==
:;frame:{{apitype|table?}} - The table handle to the named frame if it exists, else nil.

==Details==
* This function acts as a secure cache for frame name to object lookups. The first call to this function will cache the frame object registered assigned to <code>name</code> in the global namespace, and all subsequent calls thereafter will return the same frame even if the global is later replaced.
* This function will not cache frame objects if the queried name does not match their actual object name as returned by [[API UIObject GetName|UIObject:GetName()]].
* If called securely, this function returns the frame to the caller untainted.

==Patch changes==
* {{Patch 2.4.3|note=Added.}}
```