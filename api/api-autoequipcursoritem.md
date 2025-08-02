# API AutoEquipCursorItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Equips the item currently held by the cursor.
 AutoEquipCursorItem()

==Example==
<syntaxhighlight lang="lua">
PickupContainerItem(0,1)
AutoEquipCursorItem()
</syntaxhighlight>

===Result===
Equips the first item in your backpack to the relevant slot (if it can be equipped).
```