# API GetQuestIndexForWatch

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the quest log index of a watched quest.
 questIndex = GetQuestIndexForWatch(watchIndex)

==Arguments==
:;watchIndex:{{apitype|number}} - The index of a quest watch; an integer between <code>1</code> and <code>[[API_GetNumQuestWatches|GetNumQuestWatches]]()</code>.

==Returns==
:;questIndex:{{apitype|number}} - The quest log's index of the watched quest.

==Caveats==
This function can return <code>nil</code> for valid <code>watchIndex</code> values if the watched quest isn't yet in the client cache. This can happen when logging in after clearing the cache.
```