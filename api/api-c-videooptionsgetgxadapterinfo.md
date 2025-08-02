# API C VideoOptions.GetGxAdapterInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info about the system's graphics adapter.
 adapters = C_VideoOptions.GetGxAdapterInfo()

==Returns==
:;adapters:structure - GxAdapterInfoDetails[]
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || e.g. "NVIDIA GeForce GTX 1060GB"
|-
| isLowPower || {{apitype|boolean}} || 
|-
| isExternal || {{apitype|boolean}} || whether the adapter is external
|}

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```