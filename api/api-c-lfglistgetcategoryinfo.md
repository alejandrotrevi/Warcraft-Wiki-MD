# API C LFGList.GetCategoryInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a specific category. Each category can contain many [[API_C_LFGList.GetActivityGroupInfo|activitiy groups]], which can contain many [[API_C_LFGList.GetActivityInfo|activities]].
 name, separateRecommended, autoChoose, preferCurrentArea = C_LFGList.GetCategoryInfo(categoryID)

==Arguments==
:;categoryID : <span class="apitype">number</span> - The categoryID of the category you want to query. Use [[API_C_LFGList.GetAvailableCategories|C_LFGList.GetAvailableCategories]]() to get a list of all available categoryIDs.

==Returns==
:;name:<span class="apitype">string</span> - The name of the category.
:;separateRecommended:<span class="apitype">boolean</span>
:;autoChoose:<span class="apitype">boolean</span>
:;preferCurrentArea:<span class="apitype">boolean</span>
```