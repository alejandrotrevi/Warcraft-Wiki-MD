# API HasExtraActionBar

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns whether the player currently has an extra action bar/button.
 hasBar = HasExtraActionBar()

==Returns==
:;hasBar:{{apitype|boolean}} - 1 if the player currently has an extra action bar (button); nil otherwise.

==Details==
* This is equivalent to the [extrabar] [[macro conditional]].

==Patch changes==
* {{Patch 4.3.0|note=Added.}}

==See also==
* {{api|GetExtraBarIndex}}
* {{api|t=e|UPDATE_EXTRA_ACTIONBAR}}
```