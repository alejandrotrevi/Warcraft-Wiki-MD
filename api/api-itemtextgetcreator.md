# API ItemTextGetCreator

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of the character who created the item text.
 creatorName = ItemTextGetCreator()

==Returns==
:;creatorName:{{apitype|string?}} - If this item text was created by a player (i.e. Saved mail message) then return their name, otherwise return nil.

==Details==
: This is available once the {{api|t=e|ITEM_TEXT_BEGIN}} event has been received.
```