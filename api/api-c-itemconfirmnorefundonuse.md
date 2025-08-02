# API C Item.ConfirmNoRefundOnUse

**Contributor:** KyrosKrane

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}} 
When a user purchases a refundable item from a vendor with an on-use effect (such as a toy or cosmetic) and attempts to use that item, the game will pop up a [[Creating simple pop-up dialog boxes|StaticPopup]] dialog informing the user that the item would no longer be refundable. If the user clicks the Okay button to continue using the item, this function confirms the use and dismisses the dialog.

 C_Item.ConfirmNoRefundOnUse()

==Patch changes==
* {{Patch 11.0.5|note=Briefly marked as Protected, then reverted shortly after.}}
```