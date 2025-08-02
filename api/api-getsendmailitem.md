# API GetSendMailItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an item attached in the outgoing message.
 name, itemID, texture, count, quality = GetSendMailItem(index)

==Arguments==
:;index:{{apitype|number}} - The index of the attachment to query, in the range of [1,ATTACHMENTS_MAX_SEND]

==Returns==
:;name:{{apitype|string}} - The localized name of the item
:;itemID:{{apitype|number}} - Numeric ID of the item
:;texture:{{apitype|fileID}} - The icon texture for the item
:;count:{{apitype|number}} - The number of items in the stack
:;quality:{{apitype|Enum.ItemQuality}} - The quality index of the item

==Example==
The following code will loop over all the items currently attached to the send mail frame, and print information about them to the chat frame:

 for i = 1, ATTACHMENTS_MAX_SEND do
    local name, itemID, texture, count, quality = GetSendMailItem(i)
    if name then
       -- Construct an [[UI_escape_sequences#Textures|inline texture sequence]]:
       print("You are sending", "\124T"..texture..":0\124t", name, "x", count)
    end
 end

==Details==
* Requires that the mailbox window is open.
* ATTACHMENTS_MAX_SEND is defined in Constants.lua, and currently (Jan 2014) has a value of 12. Using this variable instead of a hardcoded 12 is recommended in case Blizzard changes the maximum number of items that may be attached to a single message.
* As of 2.3.3 this function is bugged and the quality is always returned as -1. If you need to know the item's quality, get a link for the item using {{api|GetSendMailItemLink}}, and pass the link to {{api|GetItemInfo}}.

==Patch changes==
* {{Patch 7.0.3|note=itemID return added between name and texture.}}

==See also==
* {{api|GetSendMailItemLink}}
* {{api|GetInboxItem}}
* {{api|GetInboxItemLink}}
```