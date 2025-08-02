# API C Transmog.GetItemInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns how an item can interact with [[transmogrification]].
 canBeChanged, noChangeReason, canBeSource, noSourceReason = C_Transmog.GetItemInfo(itemID)

== Arguments ==
; itemID : <span class="apitype">number</span> - ID of the item to query.

== Returns ==
; canBeChanged : <span class="apitype">boolean</span> - true if the item can be transmogrified to look like another.
; noChangeReason : String/nil - if the item cannot be transmogrified, a token identifying the reason; otherwise nil.
:* "INVALID_TYPE" : items of this type cannot be transmogrified (e.g. fishing poles, or non-equippable items)
:* "NO_ITEM" : player does not have the item.
; canBeSource : <span class="apitype">boolean</span> - true if the appearance of this item can be transferred to another.
; noSourceReason : String/nil - if the item cannot be used to transmogrify another, a token identifying the reason; otherwise nil.

== See also ==
* {{api|CanTransmogrifyItemWithItem}}

==Patch changes==
* {{Patch 7.0.3|note=Moved from {{api|GetItemTransmogrifyInfo}} to {{api|C_Transmog.GetItemInfo}}.}}
```