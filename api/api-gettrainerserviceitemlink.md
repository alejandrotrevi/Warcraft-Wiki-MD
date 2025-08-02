# API GetTrainerServiceItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns an item link for a trainer service.
 link = GetTrainerServiceItemLink(index)

==Arguments==
:;index:{{apitype|number}} - Index of the trainer service to a link for.

==Returns==
:;link:{{apitype|string}} : [[ItemLink]] - The item link for the given trainer service.

==Details==
* Indices are affected by the trainer filter. (See [[API_GetTrainerServiceTypeFilter|GetTrainerServiceTypeFilter]] and [[API_SetTrainerServiceTypeFilter|SetTrainerServiceTypeFilter]].)
```