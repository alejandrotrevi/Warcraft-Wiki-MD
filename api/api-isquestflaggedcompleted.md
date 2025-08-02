# API IsQuestFlaggedCompleted

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Determine if a quest has been completed.  
 isCompleted = IsQuestFlaggedCompleted(questID)

==Arguments==
:;questID:{{apitype|number}} - The quest to query.

==Returns==
:;isCompleted:{{apitype|boolean}} - true if it is completed, false if not or if the questID is not valid.

==Example==

 print(IsQuestFlaggedCompleted(30041))  -- For a Pandaren
 true
 print(IsQuestFlaggedCompleted(13485))  -- The Panda has not Honored the Borean Tundra flame. 
 false

==See also==
* {{api|GetQuestsCompleted}}

==Patch changes==
* {{Patch 6.0.2|note= Now returns true or false}}
```