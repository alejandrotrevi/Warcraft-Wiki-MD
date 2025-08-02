# API AcceptSockets

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Confirms pending gems for socketing.
 AcceptSockets()

==Details==
* The socketing API designates a single item ({{api|SocketInventoryItem}}, {{api|SocketContainerItem}}) to be considered for socketing at a time. While an item is being considered for socketing, players may drop new gems into its sockets ({{api|ClickSocketButton}}). If the user wishes to actually perform the socketing, AcceptSockets() must be called to confirm.
* There is no dedicated API call to ''reject'' a tentative socketing, although you may use {{api|CloseSocketInfo}}() to exit socketing without making any changes to item. You can then select the item for socketing again.
* Replaces existing gems if necessary.

==See also==
* {{api|SocketInventoryItem}}, {{api|SocketContainerItem}}
* {{api|ClickSocketButton}}
* {{api|CloseSocketInfo}}
```