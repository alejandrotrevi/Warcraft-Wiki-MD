# API ItemTextPrevPage

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Moves to the previous page of the item text.
 ItemTextPrevPage()

==Details==
: This simply requests the previous page, you will receive an ITEM_TEXT_READY event when the new page is ready.

: Try only to call this after receiving an ITEM_TEXT_READY event for the current page, and dont call it IN the event handler for that event, things get a little odd (Looks like a synchronization issue in the client) and your page cache might get corrupted.

: Does nothing if called while viewing the first page.
```