# API CheckInbox

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Queries the server for mail.
 CheckInbox()

==Details==
* This function requires that the mailbox window is open.
* After it is called and the inbox populated, the client's stored mailbox information can be accessed from anywhere in the world. That is, functions like {{api|GetInboxHeaderInfo}}() and {{api|GetInboxNumItems}}() may be called from anywhere. Note that only the *stored* information can be accessed -- to get current inbox info, you have to call CheckInbox() again.
```