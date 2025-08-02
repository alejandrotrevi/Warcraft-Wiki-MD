# API C InterfaceFileManifest.GetInterfaceArtFiles

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_InterfaceFileManifest|system=InterfaceFileManifest}}
Obtains a list of all interface art file names.
 images = C_InterfaceFileManifest.GetInterfaceArtFiles()

==Returns==
:;images:{{apitype|string[]?}} - A list of file names.

==Details==
* This function always returns nil inside the [[FrameXML]] environment. It only returns a table while on Glue screens such as character selection, where addon code cannot run.

==Patch changes==
* {{Patch 10.1.7|note=Added.}}
```