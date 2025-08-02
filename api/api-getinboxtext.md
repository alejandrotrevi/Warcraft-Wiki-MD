# API GetInboxText

**Contributor:** Ddcorkum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the text of a message in the mailbox.
 bodyText, stationaryMiddle, stationaryEdge, isTakeable, isInvoice, isConsortium = GetInboxText(index)

==Arguments==
:;index:{{apitype|number}} - the index of the message (1 is the first message)

==Returns==
:;bodyText:{{apitype|string}} - the text of the message.
:;stationaryMiddle:{{apitype|string}} - the texture for the middle of the stationary.
:;stationaryEdge:{{apitype|string}} - the texture for the edge of the stationary.
:;isTakeable:{{apitype|boolean}} - whether the copy of the mail text has been taken.
:;isInvoice:{{apitype|boolean}} - not nil if the message is an auction house Invoice. see [[API GetInboxInvoiceInfo|GetInboxInvoiceInfo()]]
:;isConsortium:{{apitype|boolean}} - indicates the message relates to crafting work orders. see [[API C_Mail.GetCraftingOrderMailInfo|C_Mail.GetCraftingOrderMailInfo()]]

==Patch changes==
* {{Patch 10.0.2|note=Return value ''isConsortium'' added.}}
```