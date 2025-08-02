# API C UI.Reload

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|hwevent}}
Reloads the User Interface.
 C_UI.Reload()

==Details==
* Reloading the interface saves the current settings to disk, and updates any addon files previously loaded by the game. In order to load new files (or addons), the game must be restarted.
* You can also use the [[MACRO_reload|/reload]] slash command; or the console equivalent: {{api|t=c|reloadUI|/console ReloadUI}}

==Patch changes==
* {{Patch 7.2.5|note=Moved to {{api|C_UI.Reload}}. The previous alias is still available as a script wrapper. [https://www.townlong-yak.com/framexml/8.1.5/Util.lua#132]}}
```