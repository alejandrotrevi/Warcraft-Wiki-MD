# API ItemTextGetMaterial

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the material texture for the item text.
 materialName = ItemTextGetMaterial()

==Returns==
:;materialName:{{apitype|string}} - The name of the material to use for displaying the item text. If nil then the material is "Parchment".

==Details==
* This is used one the {{api|t=e|ITEM_TEXT_READY}} event has been received for a page.
* See FrameXML/ItemTextFrame.lua for examples of how the material is used to select a set of textures.
```