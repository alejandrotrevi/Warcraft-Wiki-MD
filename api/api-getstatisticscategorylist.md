# API GetStatisticsCategoryList

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the list of statistic categories.
  categories = GetStatisticsCategoryList()

==Returns==
:;categories:{{apitype|table}} - list of all the categories

==Example==
The snippet below prints info about the category IDs.
 local categories = GetStatisticsCategoryList()
 for i, id in next(categories) do
     local key, parent = GetCategoryInfo(id)
     print("The key %d has the parent %d", key, parent)
 end

==Patch changes==
* {{Patch 3.0.2|note=Added.}}
```