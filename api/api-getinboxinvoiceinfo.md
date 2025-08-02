# API GetInboxInvoiceInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an auction house invoice.
 invoiceType, itemName, playerName, bid, buyout, deposit, consignment = GetInboxInvoiceInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of the message, starting from 1.

==Returns==
:;invoiceType:{{apitype|string?}} - One of "buyer", "seller" or "seller_temp_invoice"; or nil if there is no invoice.
:;itemName:{{apitype|string?}} - The name of the item sold/bought, or nil if there is no invoice.
:;playerName:{{apitype|string?}} - The player that sold/bought the item, or nil if there were multiple buyers/sellers involved. Will also return nil if there is no invoice.
:;bid:{{apitype|number}} - The amount of money bid on the item.
:;buyout:{{apitype|number}} - The amount of money set as buyout for the auction.
:;deposit:{{apitype|number}} - The amount paid as deposit for the auction.
:;consignment:{{apitype|number}} - The fee charged by the auction house for selling your consignment.

==Details==
* During the 1 hour delay on auction house payments, the message "Sale Pending: [item name]" may be queried with GetInboxInvoiceInfo() to determine the bid, buyout, deposit and consignment fee amounts.  This is useful, since {{api|GetInboxHeaderInfo}}() for that message (correctly) reports 0 money attached.

==Patch changes==
* {{Patch 2.1.0|note=''seller_temp_invoice'' added.}}
```