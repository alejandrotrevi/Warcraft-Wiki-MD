# API C EventUtils.NotifySettingsLoaded

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Notifies the user interface that settings are loaded and are ready to be queried.
 C_EventUtils.NotifySettingsLoaded()

==Details==
* Immediately triggers the {{api|t=e|SETTINGS_LOADED}} event.
* This function will be called after both the {{api|t=e|PLAYER_ENTERING_WORLD}} and {{api|t=e|VARIABLES_LOADED}} events have fired.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```