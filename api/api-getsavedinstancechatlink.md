# API GetSavedInstanceChatLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a hyperlink for a player's raid save.
 instanceChatLink = GetSavedInstanceChatLink(index)

==Arguments==
:;index:{{apitype|number}} - The index of the instance you want to query.

==Returns==
:;instanceChatLink:{{apitype|string}} : [[SavedInstanceChatLink]] - Returns nil if instance there is nothing to link at the index.
```