# API GetBagName

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item name of the specified player bag.
 bagName = GetBagName(index)  

==''Arguments''==
:;index:{{apitype|number}} - number of the bag the item is in, 0 is your backpack, 1-4 are the four additional bags, numbered right to left

==''Returns''==
:;bagName:{{apitype|string}} - the name of the specified bag (example "Green Woolen Bag")

==''Examples''==
 local bagName = GetBagName(0);  
 -- Returns localized "Backpack".

----
;''Result''

: bagName will contain the name of the specified bag if the bag number is 0-4 otherwise it will be nil, unless when the bank is opened, in which case GetBagName(-1) (for the bank) is nil and GetBagName(6) will give the name of the first bank bag, GetBagName(7) the name of the second bank bag, etc ...

----
;''Notes''

: It seems that there is no way to check the keyholder name; GetContainerNumSlots and GetBagName returns 32 and nil while bagID is -2.

:: GetBagName(-2) - returns nil
:: GetContainerNumSlots(-2) - always returns 32
```