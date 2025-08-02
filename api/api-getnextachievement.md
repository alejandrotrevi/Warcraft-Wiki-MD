# API GetNextAchievement

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the next achievement in a chain.
 nextID, completed = GetNextAchievement(achievementID)

==Arguments==
:;achievementID:{{apitype|number}} - The ID of the Achievement

==Returns==
:;nextID:{{apitype|number?}} - The ID of the next Achievement in chain, <code>nil</code> otherwise
:;completed:{{apitype|boolean?}} - True if the next achievement has been completed, <code>nil</code> otherwise

==Patch changes==
* {{Patch 3.0.2|note=Added.}}
```