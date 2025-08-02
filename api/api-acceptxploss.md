# API AcceptXPLoss

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Confirms the [[resurrection sickness]] and durability loss penalty on being resurrected by a spirit healer.
 AcceptXPLoss()

==Description==
*The name is misleading, originating from the WoW beta when resurrecting at a spirit healer cost [[experience]].

==Patch changes==
* {{Patch 10.0.0|note=Replaced by <code>{{api|C_PlayerInteractionManager.ConfirmationInteraction}}(Enum.PlayerInteractionType.SpiritHealer</code><sup>[https://github.com/Gethe/wow-ui-source/blob/e38db433d5af642f16454383bc67ec7c2da74d54/Interface/FrameXML/StaticPopup.lua#L2806]</sup>.}}
* {{Patch 1.1.1|note=Now results in a 25% loss in durability for a player's equipped gear and items in inventory. The length of resurrection sickness suffered from has also been decreased to a maximum of 10 minutes.}}
* {{Patch 1.1.0|note=There is no longer any experience loss, instead all items (equipped and inventory) will take 100% durability loss and the character will gain resurrection sickness for a duration that scales according to level.}}

==See also==
* [[CONFIRM_XP_LOSS]] - fired upon accepting resurrecton sickness and durability loss
* [[PLAYER_UNGHOST]] - fired upon returning to life by any source, including spirit healers
```