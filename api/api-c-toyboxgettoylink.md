# API C ToyBox.GetToyLink

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the item link for a toy.
 itemLink = C_ToyBox.GetToyLink(itemID)

==Arguments==
:;itemID:{{apitype|number}} - Numeric ID of the item.

==Returns==
:;itemLink:{{apitype|string?}} - The toy's localized [[itemLink]], or nil if that itemID is not a toy.

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```