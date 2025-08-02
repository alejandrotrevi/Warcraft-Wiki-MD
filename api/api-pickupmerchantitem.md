# API PickupMerchantItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Places a merchant item onto the cursor. If the cursor already has an item, it will be sold.
 PickupMerchantItem(index)

==Arguments==
:;index:{{apitype|number}} - The index of the item in the merchant's inventory.

==Details==
: Interesting thing is this function can be used to drop an item to the merchant as well. This will happen if the cursor already holds an item from player's bag:
 PickupContainerItem(bag, slot)
 PickupMerchantItem(0)

==Patch changes==
* As of patch 2.3 using this function to sell stacks of items does not work, instead it fails silently.  Selling unstacked items work, so unstacking and selling items one by one is an alternative. Blizzard is aware of this issue: [http://forums.worldofwarcraft.com/thread.html?topicId=2855994059#12 http://forums.worldofwarcraft.com/thread.html?topicId=2855994059#12]
```