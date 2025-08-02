# API GetNumTrackingTypes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of available tracking types for the minimap.
 GetNumTrackingTypes()

----
;''Returns''

: Number of available tracking methods. Note that it excludes the "None" option from the counting. Both spells and static tracks are counted.

----
;''Example''

Prints available tracking methods in the default chat frame:
 local count = GetNumTrackingTypes();
 DEFAULT_CHAT_FRAME:AddMessage(count);
```