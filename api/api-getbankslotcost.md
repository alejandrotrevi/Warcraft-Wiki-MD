# API GetBankSlotCost

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the cost of the next bank bag slot.
 cost = GetBankSlotCost(numSlots)

==Arguments==
:;numSlots:{{apitype|number}} - Number of slots already purchased.

==Returns==
:;cost:{{apitype|number}} - Price of the next bank slot in copper.

==Example==
The following example outputs amount of money you'll have to pay for the next bank slot:
 local numSlots,full = GetNumBankSlots();
 if full then
  print("You may not buy any more bank slots");
 else
  local c = GetBankSlotCost(numSlots);
  print(("Your next bank slot costs %d g %d s %d c"):format(c/10000, c/100 % 100, c % 100));
 end
```