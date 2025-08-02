# API TakeInboxItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Takes the attached item from the mailbox message.
 TakeInboxItem(messageIndex, attachIndex)

==Arguments==
:;messageIndex:{{apitype|number}} - the index of the mailbox message you want to take the item attachment from.
:;attachIndex:{{apitype|number}} - The index of the item to take (1-ATTACHMENTS_MAX_RECEIVE(16))

==Details==
: Sends a request to the server to take an item attachment from a mail message.  Note that this is only a request to the server, and the action might fail.  Possible reasons for failure include that the users bags are full, that they already have the maximum number of the item they are allowed to have (eg, a unique item), or that a prior TakeInboxItem() request is still being processed by the server.  There may be other reasons for failure.Would attempt to take the attachment from the first message in the Inbox and place it in the next available container slot.
```