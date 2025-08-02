# API C Item.DoesItemExist

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Item|system=Item}}
Needs summary.
 itemExists = C_Item.DoesItemExist(emptiableItemLocation)
            = C_Item.DoesItemExistByID(itemInfo)

==Arguments==
===<font color="#4ec9b0">DoesItemExist</font>===
:;emptiableItemLocation:{{apitype|ItemLocationMixin}}
===<font color="#4ec9b0">DoesItemExistByID</font>===
:;itemInfo:{{apitype|number,string}} : {{:ItemInfo}}

==Returns==
:;itemExists:{{apitype|boolean}}

==See also==
* [https://github.com/Stanzilla/WoWUIBugs/issues/449 WoWUIBugs #449] '''C_Item.DoesItemExistByID() always returns true'''
```