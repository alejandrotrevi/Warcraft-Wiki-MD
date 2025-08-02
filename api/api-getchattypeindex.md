# API GetChatTypeIndex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the index for a chat type.
 index = GetChatTypeIndex(messageGroup)

==Arguments==
:;messageGroup:{{apitype|string}} - The type code for the chat type (One of the key values of the '''[[ChatTypeInfo]]''' table).

==Returns==
:;index:{{apitype|number}} - The numeric type index for that chat type, used as the ID number for coloring.
```