# API GetQuestItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link for a required/reward/choice quest item.
 itemLink = GetQuestItemLink(type, index)

==Arguments==
:;type:{{apitype|string}} - "required", "reward" or "choice"
:;index:{{apitype|number}} - Quest reward item index.

==Returns==
:;itemLink:{{apitype|string}} - The [[ItemLink]] to the quest item specified.

==Example==
<syntaxhighlight lang="lua">
local link = GetQuestItemLink("choice", 1);
print(link)
-- |cff9d9d9d|Hitem:7073:0:0:0:0:0:0:0|h[Broken Fang]|h|r
</syntaxhighlight>
```