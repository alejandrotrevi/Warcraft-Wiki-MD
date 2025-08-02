# API GetInboxItem

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an item attached to a message in the mailbox.
 name, itemID, texture, count, quality, canUse  = GetInboxItem(index, itemIndex)

==Arguments==
:;index:{{apitype|number}} - The index of the message to query, in the range [1,[[API_GetInboxNumItems|GetInboxNumItems()]]]
:;itemIndex:{{apitype|number}} - The index of the item to query, in the range [1,ATTACHMENTS_MAX_RECEIVE]

==Returns==
:;name:{{apitype|string}} - The localized name of the item
:;itemID:{{apitype|number}} - Numeric ID of the item.
:;texture:{{apitype|string}} - The path to the icon texture for the item
:;count:{{apitype|number}} - The number of items in the stack
:;quality:{{apitype|number}} - The [[API_TYPE_Quality|quality index]] of the item
:;canUse:{{apitype|boolean}} - 1 if the player can use the item, or nil otherwise

==Example==
Loop over all messages currently in the player's mailbox, get information about the items attached to them, and print it to the chat frame:
<syntaxhighlight lang="lua">
 for i = 1, GetInboxNumItems() do
    -- An underscore is commonly used to name variables you aren't going to use in your code:
    local _, _, sender, subject, _, _, _, hasItem = GetInboxHeaderInfo(i)
    if hasItem then
       print("Message", subject, "from", sender, "has attachments:")
       for j = 1, ATTACHMENTS_MAX_RECEIVE do
          local name, itemID, texture, count, quality, canUse = GetInboxItem(i, j)
          if name then
             -- Construct an [[UI_escape_sequences#Textures|inline texture sequence]]:
             print("\128T"..texture..":0\128t", name, "x", count)
          end
       end
    else
       print("Message", subject, "from", sender, "has no attachments.")
    end
 end
</syntaxhighlight>

==Details==

* As of 2.3.3 this function is bugged and the quality is always returned as -1. If you need to know the item's quality, get a link for the item using {{api|GetInboxItemLink}}, and pass the link to {{api|GetItemInfo}}.

==Patch changes==
* {{Patch 7.0.3|note=itemID return added between name and texture.}}

==See also==

* {{api|GetInboxItemLink}}
* {{api|GetSendMailItem}}
* {{api|GetSendMailItemLink}}
```