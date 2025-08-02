# API C Ping.GetDefaultPingOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Ping|system=PingManager}}
Needs summary.
 pingTypes = C_Ping.GetDefaultPingOptions()

==Returns==
:;pingTypes:{{apitype|PingTypeInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| orderIndex || {{apitype|number}} || 
|-
| type || {{apitype|Enum.PingSubjectType}} || 
|-
| uiTextureKitID || {{apitype|textureKit}} || 
|}

{{:Enum.PingSubjectType}}

==Patch changes==
* {{Patch 10.2.5|note=Moved to C_Ping namespace and no longer forbidden.}}
* {{Patch 10.1.7|note=Added.}}
```