# API GetInboxHeaderInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for a message in the mailbox.
 packageIcon, stationeryIcon, sender, subject, money, CODAmount, daysLeft, hasItem, wasRead, wasReturned, textCreated, canReply, isGM = GetInboxHeaderInfo(index)

==Arguments==
:;index:{{apitype|number}} - the index of the message (ascending from 1).

==Returns==
:;packageIcon:{{apitype|string}} - texture path for package icon if it contains a package (nil otherwise).
:;stationeryIcon:{{apitype|string}} - texture path for mail message icon.
:;sender:{{apitype|string}} - name of the player who sent the message.
:;subject:{{apitype|string}} - the message subject.
:;money:{{apitype|number}} - The amount of money attached.
:;CODAmount:{{apitype|number}} - The amount of COD payment required to receive the package.
:;daysLeft:{{apitype|number}} - The number of days (fractional) before the message expires.
:;hasItem:{{apitype|number}} - Either the number of attachments or nil if no items are present.  Note that items that have been taken from the mailbox continue to occupy empty slots, but hasItem is the total number of items remaining in the mailbox.  Use ATTACHMENTS_MAX_RECEIVE for the total number of attachments rather than this.
:;wasRead:{{apitype|boolean}} - 1 if the mail has been read, nil otherwise.  Using [[API GetInboxText|GetInboxText]]() marks an item as read.
:;wasReturned:{{apitype|boolean}} - 1 if the mail was returned, nil otherwise.
:;textCreated:{{apitype|boolean}} - 1 if a letter object has been created from this mail, nil otherwise.
:;canReply:{{apitype|boolean}} - 1 if this letter can be replied to, nil otherwise.
:;isGM:{{apitype|boolean}} - 1 if this letter was sent by a GameMaster.

==Details==
* This function may be called from anywhere in the world, but will only be current as of the last time {{api|CheckInbox}} was called.
* Details of an Auction House message can be extracted with {{api|GetInboxInvoiceInfo}}.
```