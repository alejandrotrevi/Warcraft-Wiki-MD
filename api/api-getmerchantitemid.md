# API GetMerchantItemID

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}Returns the itemID of an item of the current merchant window.
 itemID = GetMerchantItemID(index)

==Arguments==
:;index:{{apitype|number}}

==Returns==
:;itemID:{{apitype|number}} - itemID of Merchant Item

==Example==
To get the itemID of an item of the current merchant window:
 /dump GetMerchantItemID(1) -- [1] = 194298
```