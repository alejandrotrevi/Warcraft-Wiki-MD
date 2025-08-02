# API GetGuildBankItemLink

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link for a guild bank slot.
 itemLink = GetGuildBankItemLink(tab,slot)

==Arguments==
:;tab:{{apitype|number}} - The index of the tab in the guild bank
:;slot:{{apitype|number}} - The index of the slot in the provided tab.

==Returns==
:;itemLink:{{apitype|string}} - The item link for the item. Returns nil if there is no item.
```