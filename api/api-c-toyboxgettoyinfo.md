# API C ToyBox.GetToyInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns toy info.
 itemID, toyName, icon, isFavorite, hasFanfare, itemQuality = C_ToyBox.GetToyInfo(itemID)

==Arguments==
:;itemID:{{apitype|number}} - The itemID returned from {{api|C_ToyBox.GetToyFromIndex}}(); possible values listed at [[ToyID]].

==Returns==
:;itemID:{{apitype|number}} - The Item ID of the toy.
:;toyName:{{apitype|string}} - The name of the toy.
:;icon:{{apitype|number}} - The icon texture ([[FileID]]).
:;isFavorite:{{apitype|boolean}} - Whether the toy is set to favorite.
:;hasFanfare:{{apitype|boolean}} - Shows a highlight for the toy.
:;itemQuality:{{apitype|Enum.ItemQuality}}

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```