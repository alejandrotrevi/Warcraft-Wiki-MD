# API GetLootRollItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Retrieves the itemlink of an item being rolled on.
 itemLink = GetLootRollItemLink(id)

==Arguments==
:;id:{{apitype|number}} - id is a number used by the server to keep track of items being rolled on.  It is generated server side and transmitted to the client.

==Returns==
:;itemLink:{{apitype|string}} : [[ItemLink]]
```