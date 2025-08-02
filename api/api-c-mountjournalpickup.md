# API C MountJournal.Pickup

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_MountJournal|system=MountJournal}}
Picks up the specified mount onto the cursor, usually in preparation for placing it on an action button.
 C_MountJournal.Pickup(displayIndex)

==Arguments==
:;displayIndex:{{apitype|number}} - Index of the mount, in the range of 1 to {{api|C_MountJournal.GetNumMounts}}() (inclusive), or 0 to pick up the "Summon Random Favorite Mount" button

==Details==
* Triggers {{api|t=e|CURSOR_UPDATE}} to indicate that the contents of the cursor have changed
* Triggers {{api|t=e|ACTIONBAR_SHOWGRID}} to indicate that the outlines of empty action bar buttons are now being displayed
* Does nothing if the specified index is out of bounds or belongs to a mount that the player has not collected.
* When a mount is on the cursor, {{api|GetCursorInfo}}() returns <code>"mount", <mountActionID></code> where <mountActionID> is the same as the second value returned by {{api|GetActionInfo}}() for an action button containing the same mount.
* When the "Summon Random Favorite Mount" button is on the cursor or action button, the mountActionID is 268435455.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}

==See also==
* {{api|ClearCursor}}()
* {{api|GetCursorInfo}}()
* {{api|PlaceAction}}()
```