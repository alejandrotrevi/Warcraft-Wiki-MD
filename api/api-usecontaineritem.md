# API UseContainerItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "item" action type of [[SecureActionButtonTemplate]] or the [[MACRO cast|/use]] slash command.}}
Uses an item from a container depending on the situation.
 UseContainerItem(bagID, slot [, target[, reagentBankAccessible]])

==Arguments==
:;bagID:{{apitype|number}} - The [[bagID|bag id]], where the item to use is located
:;slot:{{apitype|number}} - The slot in the bag, where the item to use is located
:;target:{{apitype|string?}} : [[UnitId]] - The unit the item should be used on. If omitted, defaults to "target" if a the item must target someone.
:;reagentBankAccessible:{{apitype|boolean?}} - This indicates, for cases where no target is given, if the item reagent bank is accessible (so bank frame is shown and switched to the reagent bank tab).

==Details==
* Slots in the bags are listed from left to right, top to bottom.  A 16 slot bag has the following slot numbers:
{| ! style="width: 150px; text-align: right; border: 1px solid #888; margin-left: 2em"
|-
| 1 || 2 || 3 || 4 
|-
| 5 || 6 || 7 || 8
|-
| 9 || 10 || 11 || 12
|-
| 13 || 14 || 15 || 16 
|}
: A 6 slot bag has the following slot numbers:
{| style="width: 150px; text-align: right; border: 1px solid #888; margin-left: 2em"
|-
|   ||   || 1 || 2
|-
| 3 || 4 || 5 || 6 
|}
* This function is protected, though may still be called in the following situations:
** When the (Guild/Reagent) Bank is open: Move the item to/from the (Guild/Reagent) Bank.
** When the Merchant frame is open: Sell the item.
** When the Mail frame is open and on the "Send Mail" tab: Add the item to the attachments.
** When the item is equippable: Equip the item.
** When the slot is empty: Do nothing.
** When the item is a locked Lockbox: Show an error message that says it's locked.
** When the item is a container (Clam Shell, Unlocked Lockbox, etc.): Open the Loot frame and show the contents.
** When the item is a book: Open the book's Gossip frame for reading.
** When the item is not a usable item: Do nothing.
** When the item starts a quest: Open the quest Gossip frame for reading.
** When the Trade frame is open: Add the item to the list of items to be traded. (I have not confirmed this)
** When the Auctions tab is open: Add item for auction pricing and submission.

==Patch changes==
* {{Patch 6.0.2|note=Protected.}}
* {{Patch 2.0.1|note=Protected.}}
```