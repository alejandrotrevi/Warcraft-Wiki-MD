# API CanShowAchievementUI

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns if the AchievementUI can be displayed.
 canShow = CanShowAchievementUI()

==Returns==
:;canShow:{{apitype|boolean}} - <code>true</code> if the achievement data is available (and hence the AchievementUI can be displayed), <code>false</code> otherwise.

==Details==
* This function returns <code>false</code> if called while the player is logging in (but not on subsequent UI reloads).
* Achievement completion data is streamed to the client when the character logs in.
* The streaming process is indicated by {{api|t=e|RECEIVED_ACHIEVEMENT_LIST}} events and generally completes before {{api|t=e|PLAYER_LOGIN}}.

==Patch changes==
* {{Patch 3.0.2|note=Added.}}
```