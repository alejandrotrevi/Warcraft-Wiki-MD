# API DeleteInboxItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}__NOTOC__
Requests the server to remove a mailbox message.
 DeleteInboxItem(index)

==Arguments==
:;index:{{apitype|number}} - the index of the message (1 is the first message)

==Details==
* DeleteInboxItem() returns immediately but one must listen for {{api|t=e|MAIL_INBOX_UPDATE}}.
* The asynchronous request may fail for different reasons, such as an invalid index or when another deletion request is already in progress
* DeleteInboxItem() is an unconditional request; the server does not check whether the message still has an item or money attached.
** The confirmation box that appears in game for these conditions is instead triggered by {{api|InboxItemCanDelete}} before calling DeleteInboxItem.
** Note that InboxItemCanDelete is not a permission-checking function, it is just an API for determining whether a message is returnable (and thus has a misleading name).  All messages are in fact deletable.
```