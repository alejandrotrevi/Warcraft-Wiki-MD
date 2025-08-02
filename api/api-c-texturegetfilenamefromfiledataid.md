# API C Texture.GetFilenameFromFileDataID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a string representing a file ID.
 filename = C_Texture.GetFilenameFromFileDataID(fileDataID)

==Arguments==
:;fileDataID:{{apitype|number}} - The file ID to query.

==Returns==
:;filename:{{apitype|string}} - A string of the form "FileData ID {fileDataID}".

==Details==
* This appears to mirror the return value of {{api|t=w|TextureBase:GetTextureFilePath}}.

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```