# API BuyMerchantItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Buys an item from a merchant.
 BuyMerchantItem(index[, quantity])

==Arguments==
:;index:{{apitype|number}} - The index of the item in the merchant's inventory
:;quantity:{{apitype|number?}} - Quantity to buy.

==Details==
If the item is sold in stacks, the quantity specifies how many stacks will be bought.

As of 4.1, the quantity argument behavior is different:
* If you do not specify quantity and the item is sold in stacks it will buy a stack.
* If you specify quantity it will buy the specified amount, sold in stacks or not.

The only limitation is the maximum stack allowed to buy from the merchant at one time, you can check this with the [[API GetMerchantItemMaxStack|GetMerchantItemMaxStack]] function.
```