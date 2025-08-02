# API C ToyBox.GetToyFromIndex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a toy by index.
 itemID = C_ToyBox.GetToyFromIndex(index)

==Arguments==
:;index:{{apitype|number}} - Ranging from 1 to {{api|C_ToyBox.GetNumFilteredToys}}.

==Returns==
:;itemID:{{apitype|number}} - The Item ID of the toy. Returns <code>-1</code> if the index is invalid.
```