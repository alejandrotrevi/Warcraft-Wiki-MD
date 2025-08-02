# API GetGraphicsAPIs

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the supported graphics APIs for the system, D3D11_LEGACY, D3D11, D3D12, etc.
 cvarValues, ... = GetGraphicsAPIs()

==Returns==
(variable returns: cvarValue1, cvarValue2, ...)
:;cvarValues:{{apitype|string}} - a value for [[CVar gxApi]].

{| class="sortable darktable zebra"
! Value !! Description
|-
| D3D11_LEGACY || Old single-threaded rendering backend using DirectX 11
|-
| D3D11 || New multi-threaded rendering backend using DirectX 11
|-
| D3D12 || Multi-threaded rendering backend using DirectX 12
|-
| metal|| 
|-
| gll || 
|-
| opengl || 
|}

==Patch changes==
* {{Patch 4.1.0|note=Added.}}

==See also==
* {{ref web|url=https://us.forums.blizzard.com/en/wow/t/new-graphics-apis-in-8-1-5/121542|author=[[Kaivax]]|date=2019-03-12|title=New Graphics APIs in 8.1.5}}
```