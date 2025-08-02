# API GetFileIDFromPath

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the FileID for an Interface file path.
 fileID = GetFileIDFromPath(filePath)

==Arguments==
:;filePath:{{apitype|string}} - The path to a game file. For example <code>Interface/Icons/Temp.blp</code>

==Returns==
:;fileID:{{apitype|number}} : [[FileID]] - The internal ID corresponding to the file path. Negative integers are temporary IDs; these are not specified in the [[CASC]] root file and may change when the client is restarted.

==Example==
<code>Interface/</code> path
 /dump GetFileIDFromPath("Interface/Icons/Temp") -- 136235

Custom file path
 /dump GetFileIDFromPath("Interface/testimg.jpg") -- -1163
 /dump GetFileIDFromPath("hello/test.jpg")        -- -2

==Patch changes==
* {{Patch 8.2.0|note=No longer works for non-interface Blizzard file paths. <ref>#wowuidev 2019-04-23 https://infobot.rikers.org/%23wowuidev/20190423.html.gz</ref>}}
* {{Patch 7.0.3|note=Added.}}

==References==
```