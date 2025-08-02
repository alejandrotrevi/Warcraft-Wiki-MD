# API C Ping.GetTextureKitForType

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Summary description.
 uiTextureKitID = C_Ping.GetTextureKitForType(type)

==Arguments==
:;type:{{apitype|Enum.PingSubjectType}} - The type of the Ping, e.g. <code>2</code> for "Assist" and <code>3</code> for "OnMyWay" Pings.
{{:Enum.PingSubjectType|nocaption=1}}

==Returns==
:;uiTextureKitID:{{apitype|textureKit}} - Name of a texture kit for the Ping.

==Patch changes==
* {{Patch 10.2.5|note=Moved to C_Ping namespace and no longer forbidden.}}
* {{Patch 10.1.7|note=Added.}}
```