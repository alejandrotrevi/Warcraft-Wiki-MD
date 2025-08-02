# API GetSendMailItemLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link of an item attached in the outgoing message.
 itemLink = GetSendMailItemLink(attachment)

==Arguments==
:;attachment:{{apitype|number}} - The index of the attachment to query, in the range of [1,ATTACHMENTS_MAX_SEND]

==Returns==
:;itemLink:{{apitype|string}} : [[ItemLink]] - The item link for the specified item

==Details==
* ATTACHMENTS_MAX_SEND is defined in Constants.lua, and currently (Jan 2014) has a value of 12. Using this variable instead of a hardcoded 12 is recommended in case Blizzard changes the maximum number of items that may be attached to a sent message.
* There is no API function to get the total number of items attached to a sent message. If your addon needs to know how many attachment slots are filled, you must loop over all the slots and count them yourself:

 local total = 0
 for i = 1, ATTACHMENTS_MAX_SEND do
    if GetSendMailItemLink(i) then
       total = total + 1
    end
 end
 print("Attachment slots used:", total, "of", ATTACHMENTS_MAX_SEND)

==See also==
* {{api|GetSendMailItem}}
* {{api|GetInboxItem}}
* {{api|GetInboxItemLink}}
```