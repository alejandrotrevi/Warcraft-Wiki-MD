# API GetExtraBarIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the action bar page containing the extra bar/button.
 extraPage = GetExtraBarIndex()

==Returns==
:;extraPage:{{apitype|number}} - index of the action bar page containing the extra action button.

==Example==
The following snippet prints out the name of your current extra button ability:
 if HasExtraActionBar() then
  local page = GetExtraBarIndex()
  local id = 1
  local slot = id + (page - 1) * NUM_ACTIONBAR_BUTTONS
  local action, id = GetActionInfo(slot)
  if action == "spell" then
   print("Your extra ability is: " .. GetSpellInfo(id))
  else
   print("The thing on your extra action button is not a spell. How odd.")
  end
 else
  print("You don't have an extra bar at the moment.")
 end

==Patch changes==
* {{Patch 4.3.0|note=Added.}}

==See also==
* {{api|HasExtraActionBar}}
```