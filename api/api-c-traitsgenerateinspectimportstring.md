# API C Traits.GenerateInspectImportString

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Returns a Talent Build String for an inspected target
 importString = C_Traits.GenerateInspectImportString(target)

==Arguments==
:;target:{{apitype|string}} : [[UnitId]] - For example <code>"target"</code>

==Returns==
:;importString:{{apitype|string}} - the Talent Build String, or an empty string if inspect information is not available

==Details==
You must first inspect a player, before this API returns any data. You may need to defer the API call by a frame after the INSPECT_READY event.

==See also==
{{api|C_Traits.GenerateImportString}} to retrieve Talent Build Strings for the current player character.

{{apinavbox|C_Traits}}
```