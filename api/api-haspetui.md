# API HasPetUI

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if the player currently has an active (hunter) pet out.
 hasUI, isHunterPet = HasPetUI()

==Returns==
:;hasUI:{{apitype|boolean}} - <code>True</code> if the player has a pet User Interface, <code>False</code> if he does not.
:;isHunterPet:{{apitype|boolean}} - <code>True</code> if the pet is a hunter pet, <code>False</code> if it is not.

==Example==
<syntaxhighlight lang="lua">
local hasUI, isHunterPet = HasPetUI();
if hasUI then
  if isHunterPet then
    DoHunterPetStuff(); -- For hunters
  else
    DoMinionStuff(); -- For Warlock minions
  end
end
</syntaxhighlight>
```